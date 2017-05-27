# Programming Fundamentals with Scratch

## Welcome!
Welcome to our Introduction to Scratch workshop!

The goal for this workshop is to introduce you to some of the key concepts of programming through an intuitive and fun programming language called Scratch.

## What is Code?
Code is a way that we as humans can interact with machines. When we use a computer, a phone or a tablet, we are using pre-defined commands to complete tasks.

When we issue commands to computers through code, we do it in one of many programming languages. Some examples of programming languages include C, Java, JavaScript, PHP, and Ruby!

Regardless of what programming language you are using, they all share one thing in common: they are grounded in logic.

Once you start to understand the logic that underpins programming, you will find it much easier to pick up and run with new and unfamiliar programming languages.

With that in mind - we're going to introduce you today to a programming language called Scratch.

## What is Scratch?
Scratch is a programming language created by MIT where you can create your own interactive stories, animations, games, music, and art.

Because Scratch has been designed for kids, it's easy to learn and use - but most importantly, it helps you to develop logic skills that are important in learning any programming language.

Scratch teaches some of the core principles of programming:
* manipulating **variables** - chunks of compute memory - to store and retrieve data
* using **operators** including arithmetic, logic operators (and, or, not), concatenation operators (this joins sentences together), and even triginometry
* understanding **control flow** - the way computers move through stages of a program
* altering flow with **conditional statements** and **loops**
* **event handling** - writing code that responds to events like key presses and mouse clicks
* **multimedia programming** including drawing, animation, and sound

Scratch programs are built using blocks that interconnect with one another to perform tasks.

Here's a few examples of some cool things that have been built in Scratch:
[Wall Runner](https://scratch.mit.edu/projects/152384832/)

[Animations](https://scratch.mit.edu/projects/94311916/)

[8-Bit Music Maker](https://scratch.mit.edu/projects/87829696/)

## Getting started with Scratch
Is super easy - just head over to: https://scratch.mit.edu/. We'll start by signing up for an account.

Once you've signed up, click 'create'!

## The Scratch Environment
There are a couple of key blocks to look at: **Events**, **Motion**, and **Control**. These blocks allow you to control the sprite, or sprites you have on the screen. The interface is broken up into a few important areas:

### Stage
The main area where information is displayed / stuff happens. Usually to start a program running, you click the green flag.

### Sprites Window
Sits below the stage, and contains a list of sprites (animated images) that you're using in your current project. We can control these sprites with our program.

### Block Palette
This section in the middle of the window contains all the programming blocks you can use. They are organized into categories, detailed below.

### Scripts Area
This section to the right of the stage contains all the programming blocks (sequences of instructions). You can drag blocks from the block palette into the scripts area to build up your scripts.

## Block Overview
Here are a couple key block types that will help you program some great projects!

### Events
Used to start a program - For example, we can make it start when you click the green flag, or when a key is pressed?

### Motion
The Motion controls are used to locate, orient, and move a sprite (their position on the stage)

### Control
The Control blocks gives you the ability to control the flow of your program. For example, should something loop 10 times? Should something only run if a certain condition is true?

### Operators
The Operators block lets you do addition, pick a random number, or check if something is greater than something else.

### Looks
The Looks block has instructions for setting the colour, size, and visibility of a sprite.

### Sensing
The sensing blocks get information from the user or some other part of the page.

### Sounds
The Sounds block let us use a sound library. You can also upload your own sounds to use in your programs.

## Building our first Scratch Project: Events
In programming, an event is a moment where something is going to happen, and what actions you'd like to take place when that event occurs.

For example: A user clicks a 'Submit Button' (event) which mails out a contact form (action).

Another example: A user clicks a hamburger menu (event), and the menu slides out (action).

An event is a *specific moment when something is going to happen* and *what actions should take place when that moment arrives*.

Let's take a look at how events work in Scratch.

### Exercise One: Walk the Walk
We're going to make our first Scratch application that makes a cat walk across the screen, ten steps at a time.

The green flag in the top corner of the Stage area - that's our event. Whenever we click that event, we'll have an action occur. What will that action be? The cat will take ten steps!

Let's plot out how we think this is going to work by writing a little bit of pseudocode. You can think of pseudocode as point form instructions that break down the steps your program will take - kind of like instructions for a recipe, or rules to a board game.

Open up a text editor of your choice - anything will do.

```
PSEUDOCODE:
1. When the green flag is clicked [Event]
2. Move the cat 10 steps [Action]
```

[Click here to see a working example!]( https://scratch.mit.edu/projects/155361643/)

### Exercise Two: Click Events
Another example of events you're likely to see when we start writing JavaScript in our projects is a click event.

Since users spend a lot of time interacting with our webpage using the mouse, it's incredibly helpful to 'listen' for these click events, and have some action fire in response. For example, when the user clicks a hamburger menu, maybe it pops out from the side of the screen.

Let's make a second animation sequence - this time, when you click Scratch (that's the cat's name, by the way), let's make it glide 100 pixels to the right (X:100), and then say something.

```
PSEUDOCODE
1. When Scratch is clicked [Event]
2. Move Scratch 100 pixels on the X axis [Action]
3. Have Scratch say 'Hello!' [Action]
```

[Click here to see a working example!](https://scratch.mit.edu/projects/155362264/)

## Loops
A loop is a piece of code that repeats multiple times.

Loops can run as little as twice or as many as an infinite number of times, repeating the same sequence of actions over again.

Let's say we want Scratch to move on his own without having to click the green button every time - we can use a loop for this.

### Exercise Three: Click and Move... Forever!
When we look at our cat moving around the page, you'll notice that we have to click the green flag every single time we want it to move forward. With loops, we can click the green flag once and have our cat move forever!

```
PSEUDOCODE
1. When the green flag is checked [Event]
2. Run the following actions forever: [Loop]
3. Move the cat 100 pixels on the X axis [Action]
4. Say hello [Action]
5. (back to step 3) [End of the Loop]
```

You'll notice that Scratch gets stuck on the edge of the stage once he runs out of real estate. How can we fix this?

[Click here to see a working example!](https://scratch.mit.edu/projects/155362675/)


## Control Flow
'Control flow' is the name we give in programming to the process of allowing our programs to have more than one possible path and outcomes.

Remember reading choose your own adventure books as a kid? The reader has control over the destiny of your story. You could determine the fate of the characters by deciding which path to pursue.

Programs work the same way - a program with only one possible outcome is about as flat as a choose your own adventure with only one path.

Currently, our cat mindlessly makes its way towards the edge of the and only stops when it can no longer go any further.

```
PSEUDOCODE:
1. When green flag is clicked [Event]
2. Run the following actions for ever: [Loop]
3. If the cat is touching the boundary [Control Flow/Conditional Statement] of the visible area
4. Say 'Ouch!' [Action]
6. Go back to step 3 [End of Loop]
```

[Click here to see a working example!](https://scratch.mit.edu/projects/155366029/)

### Putting it all Together: Building a Maze
So far we've learned about events, loops, and control flow. Let's put it all together to build a simple maze.



Let's start by taking a look at the finished project:

https://scratch.mit.edu/projects/155367201/

The first thing that we're going to need to do is decide what our maze is going to look like. Let's draw this out by hand through a process called *wireframing*.

Once we've wireframed the maze, let's draw it as a backdrop. We'll also draw the goal.

Let's look at our pseudocode:
```
1) When the user presses the right arrow [Event]
2) Move the sprite 10 pixels to the right [Action]
3) Repeat 1-2 for Left, Up, and Down
4) If the user moves and they hit a wall [If statement]
5) Block them from moving further. [Action]
6) If the sprite touches the goal
7) Tell them, you win!

```
Now let's delete scratch and create our own sprite that can move around.

Wireframing is like a 'blueprint' for our application. Let's wireframe the shape of the maze on a piece of paper, decide where the user will start, and where the prize will be, and make sure that they can get through the maze.

## Final Exercise
With a partner, you have one hour to build your own Scratch program - it can be whatever you want - a game, a story, an animation, whatever. At the end of the hour, you'll submit whatever you built and you and your partner will be giving quick 90 second presentations on your topic.

### Submitting Your Project
To submit your project:

1. Click the 'Share' button in the top right of the Scratch editor. 
2. This will take you to your project page. You will see a window with your project, and above it you will be given the option to change its name. Name your project with the first names of each group member - so for example if Samantha and Alex are in a group project together - they will name their project 'samantha-alex'. Do NOT forget to name your project this way.
3. Copy the URL at the top of the project page, and send it to simon@hackeryou.com

### The Presentation Component
You will only have 90 seconds to present, so use your time wisely. Take us through whatever you have built. Talk to us about a particular feature you found exciting, or a challenge you overcame. Make sure that each member of your group is given equal time to talk. One person can demo the project while the other person talks the audience through it.

Some tips for presenting:
* Make sure to project so that you can be heard in the back of the classroom
* Try to avoid speaking directly to the projector screen - make sure to make eye connect and connect with your audience
* Make sure each presenter is given EQUAL time
* Stay positive! Try to avoid using any negative or critical language as you present on your project.
* Have fun! 

## Takeaways
Scratch is a powerful tool for learning the logic that underpins a programming language like JavaScript.

Today we looked at Events, Control Flow (If statements), and Loops. Be prepared to see these concepts (and more) when we dive into JS!

## Survey
[We have a small survey we'd love if you could complete](https://docs.google.com/forms/d/1thokMMCzzCNdmWwBlMsk_SKjCLLi4Z0kLhZDe_DTWoE/edit?usp=sharing)
