# Programming Fundamentals with Scratch

# Welcome!
Today's goal: introducing you to the fundamental concepts of code and programming through Scratch.

# Warmup: Bingo Cards

# What is Code?
Code is a way that we as humans can interact with machines. When we use a computer, a phone or a tablet, we are using pre-defined commands to complete tasks.

In the first few weeks of the bootcamp, we'll be focusing on HTML and CSS, tools that describe the structure and design of your website. 

After that, we'll dive into the world of JavaScript, which is more focused on your website's functionality (how a user interacts with it - whether it's a form, a gallery of sliding images, or a modal that pops up and prompts a user to sign up for a newsletter).

In order to get you comfortable with some of the fundamental concepts of programming, we're gonna look at them through a language called Scratch!

## What is Scratch?
Scratch is a programming language where you can create your own interactive stories, animations, games, music, and art.

Because Scratch has been designed for kids, it's easy to learn and use - but it still teaches some fundamental programming concepts that make up the foundation of a programming language like JavaScript. 

Ideas that show up in Scratch that you will see again in JavaScript:
* manipulating **variables** - chunks of compute memory - to store and retrieve data
* using **operators** including arithmetic, logic operators (and, or, not), concatenation operators (this joins sentences together), and even triginometry
* understanding **control flow** - the way computers move through stages of a program
* altering flow with **conditional statements** and **loops**
* **event handling** - writing code that responds to events like key presses and mouse clicks
* **multimedia programming** including drawing, animation, and sound

Scratch programs are built using blocks that interconnect with one another to perform tasks (not unlike something called **functions** in JavaScript). 

There are a couple of key blocks to look at: **Events**, **Motion**, and **Control**. These blocks allow you to control the sprite, or sprites you have on the screen. The interface is broken up into a few important areas:

## The Scratch Environment

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
The Looks blocks have instructions for setting the colour, size, and visibility of a sprite.

### Sensing
The sensing blocks get information from the user or some other part of the page.

### Sounds
The Sounds block let us use a sound library. You can also upload your own sounds to use in your programs.

## Concept 1: Events
When we say the word 'event', what comes to mind? A concert you're planning to go to, a meeting you need to be on time for, or maybe even your grandma's birthday party that you are stoked for.

When that event happens (let's take your grandma's birthday, for example), there are subsequent actions that you know come along with it: there will be a cake, presents, and you'll get some kisses on the cheek for being a good grandchild.

Events work similarly in programming. They represent a specific moment when something is going to happen (your grandma's birthday) and what actions should take place when that moment arrives (presents, cake, kisses).

Let's take a look at how events work in scratch.


## Building your first Scratch Animation

### Exercise One: Walk the Walk 
We're going to make our first Scratch application that makes a cat walk across the screen, ten steps at a time.

The green flag in the top corner of the Stage area - that's our event. Whenever we click that event, we'll have an action occur. What will htat action be? The cat will take ten steps!

```
PSEUDOCODE:
1. When the green flag is clicked, move the cat 10 steps.
```

Another example of events you're likely to see when we hit JavaScript is a click event. Since users spend a lot of time interacting with our webpage using the mouse, it's incredibly helpful to 'listen' for these click events, and have some action fire in response.

### Exercise Two: Click and move
Let's make a second animation sequence - this time, when you click the right arrow , let's make him glide 100 pixels to the right (X:100), and then say something.

```
PSEUDOCODE
1. When the green flag is clicked,
2. Move the cat 100 pixels on the X axis
3. Say 'Hello!'
```

## Concept 2: Loops
Remember the movie Groundhog Day? Bill Murray finds himself living out the same day over and over again.

This was a less than ideal situation for Bill, but is perfect for writing programs that we want to run over and over again without stopping. In programming, we call actions that repeat a 'loop'. 

Loops can run as little as twice or as many as an infinite number of times, repeating the same sequence of actions over again.

When we look at our cat moving around the page, you''ll notice that we have to click the green flag and trigger a new event every single time we want it to move forward. With loops, we can click the green flag once and have our cat move forever!

### Exercise Three: Click and Move Refactored
We're going to 'refactor' our click and move animation. Refactoring is a fancy way of basically saying 'rejig to make it work better'.

```NEW PSEUDOCODE
1. When the green flag is checked
2. Run the following actions forever:
3. Move the cat 100 pixels on the X axis
4. Say hello
5. (back to step 3)
```

## Concept 3: Control Flow
Remember reading choose your own adventure books as a kid? What made them so awesome is that they gave you, the reader, control over the destiny of your story. You could determine the fate of the characters by deciding which path to pursue.

Programs work the same way - a program with only one possible outcome is about as flat as a choose your own adventure with only one path.

'Control flow' is the name we give in programming to the process of allowing our programs to have more than one possible outcome. 

Like water encountering a human-made dam in the middle of a stream, we are controlling the 'flow' of information as it moves through our application.

Currently, our cat mindlessly makes its way towards the edge of the and only stops when it can no longer go any further. 

```
PSEUDOCODE:
1. When green flag is clicked
2. Run the following actions for ever:
3. Move the cat 100 pixels on the x axis
4. If the cat hits the boundary of the visible area
5. Turn around and go the other way
6. Go back to step 3
```

### Putting it All Together
So far we've learned about events, loops, and control flow. Let's put it all together to build a simple animation sequence. We'll make a mouse that walks over to a bowl of cheezeits and when it gets there it says yum!



### Final Exercise: Pong!



