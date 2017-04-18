# Programming Fundamentals with Scratch

## Welcome!
Welcome to our Introduction to Scratch workshop!

The goal for this workshop is to introduce you to some of the key concepts of programming through an intuitive and fun programming language called Scratch.

## Warmup: Bingo Cards
Let's start with a quick warmup!

## What is Code?
Code is a way that we as humans can interact with machines. When we use a computer, a phone or a tablet, we are using pre-defined commands to complete tasks.

You can think of code as a language that allows humans to communicate with computers. Just like a spoken language, it has words and grammar (called 'syntax') that help you to describe to the computer what you're trying to accomplish.

And what can you accomplish with code? Well, in the bootcamp, you'll learn how to use code to build webpages. But you can also use code to build desktop applications, games, and even operating systems.

And just like spoken languages, there are many different kinds of programming languages. During the bootcamp we'll be focusing specifically on JavaScript, because it is the primary language that is used to create interactivity on web pages.

What do we mean when we say interactivity? Well, if HTML and CSS describe how a website is structured and how it looks, **JavaScript describes what happens when the user interacts with it**.

This can include creating galleries that flick between images on their own, webpages that let you login and have your own account, and forms that check to make sure you've filled out all of the fields before they let you submit them. These all fall under the category of website 'functionality'.

Though languages all have different syntax, they share a lot of common logic. Once you learn this logic in one language, it will be very easy to transfer it over to another. If this is your first time learning a new programming language, you will find that your second one will take you a fraction of the time to learn.

With that in mind - we're going to introduce you today to a different kind of programming language called Scratch. While the syntax of Scratch may be different, you will find that the concepts transfer over 100% to when we start learning JavaScript. So pay close attention!

## What is Scratch?
Scratch is a programming language created by MIT where you can create your own interactive stories, animations, games, music, and art.

Because Scratch has been designed for kids, it's easy to learn and use - but it still teaches some fundamental  concepts that make up the foundation of a programming language like JavaScript.

Ideas that show up in Scratch that you will see again in JavaScript:
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
Is super easy - just head over to: https://scratch.mit.edu/ and click 'create'!

Take five to ten minutes now and just mess around it with. Don't worry, there's no way to do this wrong - just explore and see what you discover.

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
When we say the word 'event', what comes to mind? A concert you're planning to go to, a meeting you can't miss, or maybe even your grandma's birthday party that you are stoked for.

When that event happens (let's take your grandma's birthday, for example), there are subsequent actions that you know come along with it: there will be a cake, presents, and you'll get some kisses on the cheek for being a good grandchild.

Events work similarly in programming. They represent a specific moment when something is going to happen (your grandma's birthday) and what actions should take place when that moment arrives (presents, cake, kisses).

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
1. When Scratch is clicked
2. Move Scratch 100 pixels on the X axis
3. Have Scratch say 'Hello!'
```

[Click here to see a working example!] (https://scratch.mit.edu/projects/155362264/)

## Loops
Remember the movie Groundhog Day? Bill Murray finds himself living out the same day over and over again.

This was a less than ideal situation for Bill, but is perfect for writing programs that we want to run over and over again without stopping. In programming, we call actions that repeat a 'loop'.

Loops can run as little as twice or as many as an infinite number of times, repeating the same sequence of actions over again.

### Exercise Three: Click and Move... Forever!
When we look at our cat moving around the page, you'll notice that we have to click the green flag every single time we want it to move forward. With loops, we can click the green flag once and have our cat move forever!

We're going to 'refactor' our click and move animation. Refactoring is a fancy way of basically saying 'rejig to make it work better'.

```
PSEUDOCODE (REFACTORED)
1. When the green flag is checked [Event]
2. Run the following actions forever: [Loop]
3. Move the cat 100 pixels on the X axis [Action]
4. Say hello [Action]
5. (back to step 3) [End of the Loop]
```

[Click here to see a working example!](https://scratch.mit.edu/projects/155362675/)


## Control Flow
Remember reading choose your own adventure books as a kid? What made them so awesome is that they gave you, the reader, control over the destiny of your story. You could determine the fate of the characters by deciding which path to pursue.

Programs work the same way - a program with only one possible outcome is about as flat as a choose your own adventure with only one path.

'Control flow' is the name we give in programming to the process of allowing our programs to have more than one possible outcome.

Like water encountering a dam in the middle of a stream, we are controlling the 'flow' of information as it moves through our application.

Currently, our cat mindlessly makes its way towards the edge of the and only stops when it can no longer go any further.

```
PSEUDOCODE:
1. When green flag is clicked [Event]
2. Run the following actions for ever: [Loop]
----------------------------------------------------
3. If the cat is touching the boundary [Control Flow/Conditional Statement] of the visible area
4. Turn the cat around 180 degrees [Action]
----------------------------------------------------
5. Move 50 steps [Action]
6. Go back to step 3 [End of Loop]
```

[Click here to see a working example!](https://scratch.mit.edu/projects/155366029/)

### Putting it all Together: Building a Maze
So far we've learned about events, loops, and control flow. Let's put it all together to build a simple maze.

Let's start by taking a look at the finished project:

https://scratch.mit.edu/projects/155367201/

The first thing that we're going to need to do is decide what our maze is going to look like. Let's draw this out by hand through a process called *wireframing*.

Wireframing is like a 'blueprint' for our application. Let's wireframe the shape of the maze on a piece of paper, decide where the user will start, and where the prize will be, and make sure that they can get through the maze.

## Final Exercise: Pong!
Your challenge is to build a game of one player pong. The pseudocode looks something like this:

```
PSEUDOCODE
1. When the Green flag is pressed
2. Start the ball in a random place on the screen
3. Start the ball moving in a random direction
4. If the ball hits an edge of the screen, bounce in a random direction
5. If the ball hits the paddle, bounce off that to go in a random direction
6. When the mouse moves, the paddle follows the mouse on the x axis
7. Run indefinitely until the paddle touches the red line, at which point you stop
```

[Take a look at the finished code here](https://scratch.mit.edu/projects/155403648/)
