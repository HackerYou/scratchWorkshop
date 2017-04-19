# Testing in React
## What is Testing?
Testing is the process by which a code's integrity is verified.

Code integrity is determined by running a program that examines a give piece of code, executes it, and checks to see if the code's results match an expected result provided by the tester.

This 'expected result' is described in something called a test.

## What is a test?
If an exam is a way of a teacher verifying a student's understanding of the coursework, then a test is a programmer's way of verifying that its program works as expected.

A programmer writes a test based on some expected behaviour of the program, and then runs the test in order to make sure that the program is working as expected.

A single test will check to determine if a piece of an application's functionality is working as expected - a group of tests can help make sure a whole application is running as expected.

Tests are composed with other tests and act as a safety net, making sure that your code is working as you are expecting it to.

Introducing new code can make old tests fail, and are a helpful way of ensuring that new code doesn't break existing functionality in your application without you knowing it.

# What is a 'unit test'?
A unit test is a level of testing where individual 'units' or components or a software are tested. A 'unit' is the smallest testable part of software. In the case of React, we'll be talking about components.

# What is 'test driven development' (TDD)
Test driven development is a philosophy of writing code.

When you want to add functionality to your application, instead of adding it right away, you complete the following steps:

1) Add a test
Add a test that determines whether or not your new piece of functionality is working. This will invariably fail (and that's okay), since you haven't written the functionality yet!

2) Run all the tests and make sure the new one fails
If it passes, it means that the test is somehow flawed (since you haven't written the code for the new piece of functionality yet!)

3) Write the code
Now you must write the code to make your failing test pass.

4) Run your tests again
Your test show now pass - if it doesn't continue to refactor your code until it does.

5) Repeat!

## Testing in the Context of React (and the front-end)

If we were building an API, we would want to make sure that our endpoints were accessible and that they stored and retrieved data the data we wanted from our database.

We would write tests that made POST and GET requests to those endpoints, and cross-referenced them against expected responses from our API.

However, in the case of the front end, and React, we're concerned primarily with how our user interface looks and behaves. When a component is rendered on to the page, we want to make sure that the right classes are getting added to it, and that when we click on it it does what we would expect it to.

## Snapshot Testing
One way that we can test to make sure our user interface looks how we would expect it to is through something called a *snapshot test*.

Dave Ceddia's article sums up perfectly the role of a snapshot test:

"A snapshot test verifies that a piece of functionality works the same as it did when the snapshot was created."

Let's say you create a React component that lists out your favourite TV shows:

```javascript
render() {
  const favouriteShows = [
    'The Wire',
    'Westworld',
    'The Crown'
  ]
  return (
    <ul className='favourite-shows'>
      {favoriteShows.map(show => <li className='show'>{show}</li>)}
    </ul>
  )
}
```

This would render some HTML that looked like this:
```html
<ul class='favourite-shows'>
  <li class='show'>The Wire</li>
  <li class='show'>Westworld</li>
  <li class='show'>The Crown</li>
</ul>
```

You could take a 'snapshot' of this rendered HTML, store it in an external file, and cross-reference it against your actual component later.

If for some reason the two didn't match up, the test would fail - at which point you would either take a new snapshot of your component, or fix your component.

### An Example
If you re-wrote your component like this:

```javascript
render() {
  const favouriteShows = [
    'The Wire',
    'Westworld',
    'The Crown',
    'Breaking Bad'
  ]
  return (
    <ul className='favourite-shows'>
      {favoriteShows.map(show => <li className='show'>{show}</li>)}
    </ul>
  )
}
```

it will now render HTML that looked like this:
```javascript
<ul class='favourite-shows'>
  <li class='show'>The Wire</li>
  <li class='show'>Westworld</li>
  <li class='show'>The Crown</li>
  <li class='show'>Breaking Bad</li>
</ul>
```

Which, when compared against your initial snapshot that did not include Breaking Bad, will fail, because your rendered HTML fails.

You will need to update your snapshot in order to reflect the new desired behaviour of your component.

## React Snapshot Testing Using Jest
The React community has embraced the library Jest in order to handle their snapshot testing.

Dan Abramov's `create-react-app` comes baked in with Jest, but let's assume that you aren't using create-react-app for a second:

```shell
npm install --save-dev jest babel-jest babel-preset-es2015 babel-preset-react react-test-renderer
```

Now you can run tests by typing in 'jest'. If you want, you can update your `package.json`
 to run jest for you when you `npm test`:

 ```json
 // package.json
 // ...
 "scripts": {
   "test": "jest"
 }
 ```

 You'll also need to update your `.babelrc` as follows:
```json
{
  "presets": ["es2015", "react"]
}
```

## Creating your First Snapshot Test
Let's start by creating the movie list component from our example above:

```javascript
// MovieList.js
const movies = [
  'The Wire',
  'Westworld',
  'The Crown',
  'Breaking Bad'
];

export default (props) => {
  return (<ul>
    {movies.map((movie, i) => <li key={`movie-${i}`}>{movie}</li>)}
  </ul>)
}
```

Now let's make a snapshot test for our `MovieList` component - snapshot tests should always have a `.test` suffix, so we'll call this file `MovieList.test.js`:

```javascript
import React from 'react';
import MovieList from './MovieList.js';
import renderer from 'react-test-renderer';

test('It renders the MovieList component', () => {
  const component = renderer.create(
    <MovieList />
  );
  let tree = component.toJSON();
  expect(tree).toMatchSnapshot();
});
```

Now we can test this out by running `npm test`.

You should see something that looks like this:

```shell
PASS  src/MovieList.test.js
 ✓ It renders the MovieList (4ms)

Snapshot Summary
› 1 snapshot written in 1 test suite.

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   1 added, 1 total
Time:        0.108s, estimated 1s
Ran all test suites.

Watch Usage
› Press p to filter by a filename regex pattern.
› Press q to quit watch mode.
› Press Enter to trigger a test run.
```

You'll also notice that a `__snapshot__` folder has been created. Inside of it you'll see a file called `MovieList.test.js.snap`, take a look inside and this is what the code looks like:

```javascript
exports[`test It renders the MovieList 1`] = `
<ul>
  <li>
    The Wire
  </li>
  <li>
    Westworld
  </li>
  <li>
    The Crown
  </li>
  <li>
    Breaking Bad
  </li>
</ul>
`;
```

## Testing with Enzyme
Since Snapshot testing can only verify a component AFTER the code has been written, it is not a part of the TDD workflow.

Enzyme, on the other hand, can be used to apply TDD to Reac

From the Enzyme Documentation:

"Enzyme is a JavaScript Testing utility for React that makes it easier to assert, manipulate, and traverse your React Components' output."

It is NOT a unit testing framework (like Jest)

"Enzyme is a testing library to render the react component into the DOM and query the DOM tree. Jest is a unit testing framework and has a test runner, assertion library, and mocking support. Enzyme and Jest is complementary. Enzyme can be used within Jest."

### Shallow Rendering vs Deep Rendering
Enzyme gives us the ability to shallow render components as well as deep render components.

What is a shallow render? It just means that it will test the component without rendering any of its nested child components.

Again Dave Ceddia gives this example:
```js
// shallow render
<span>
  <Name person={person}/>
  <Age person={person}/>
</span>
```

```js
// deep render
<span>
  <span className="name">Dave</span>
  <span className="age">32</span>
</span>
```

Here's a sample component tested with Enzyme:

```javascript
// SearchBar
import React from 'react';

export default class SearchBar extends React.Component {
    constructor() {
        super();
        this.state = {
            inputValue: ''
        }
        this.handleChange = this.handleChange.bind(this);

    }
    handleChange(e) {
        this.setState({
            inputValue: e.target.value
        });
    }
    render() {
        return (
            <div>
                <input type="text" onChange={this.handleChange} value={this.state.inputValue} />
            </div>
        )
    }
}

// SearchBar.js
import React from 'react';
import { shallow, mount } from 'enzyme';
import SearchBar from './SearchBar.js';

test('It updates the state when the user types something in.', () => {
    const search = shallow(<SearchBar/>);
    search.find('input').simulate('change', {target: {value: 'Simon'}});
    console.log(search.state().inputValue);
    expect(search.state().inputValue).toEqual('Simon');
});

```

### What should we be testing?
When we are writing some components, here are the kinds of things we should be checking for:

* **Does our component render the correct thing?** - If we look at our MovieList component, if we pass in a list of movies will it render them properly?

* **Any updates to state inside of our component** - if the state of the component changes the ui of the component (updates the classNames, displays a modal, renders additional JSX) these need to be tested. If a button only appears when a user is logged in, for example, we want to test to make sure it doesn't appear if they aren't.

* **Events** - Anything that a user can interact with should be tested. Clicks events, change events, etc.

* **Edge Cases** - If we're going to be receiving data from an external source (like an API backend), we need to make sure our code doesn't fail if we don't get data the way we're expecting to.
