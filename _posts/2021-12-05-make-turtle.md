---
layout: post
title: "Make a Turtle!"
date: "2021-12-05 09:00:00 +0000"
author: Miles Berry
permalink: /2021/12/make-turtle/
comments: true
image:
        feature: 041221.jpg
---

The first thing on Papert and Solomon's (1971) list of twenty things
is make a turtle. Over the intervening fifty years the programmable
turtle has featured as many young people's first introduction to
programming, both on the floor and on the screen. It still has much to
commend it: it is simple enough for children to grasp the basic idea of
the robot's operation - it moves forwards or backwards; it turns to the
left or to the right; it can draw, or not draw, as it moves. The
hardware itself is simple enough too: motors for each of the main
wheels, able to turn independently, and a pen that can be raised or
lowered that fits right in the middle of these wheels: as a 'notional
machine' (Boulay et al., 1981), it seems much easier for a child to
grasp conceptually than a smartphone, a tablet or a distant website. It
is also a friendly sort of thing: it is neither too big, nor too small;
it often develops some sort of character, at least in the child's eyes;
and, crucially, the child can put herself in the turtle's place. The
humble turtle is capable of great things, and many realise they can move
on from drawing regular polygons or simple pictures to stunning, complex
geometric figures.

## Turtles all the way down

Often a child's first experience of programming, even if it's not called
that at the time, is with some sort of floor robot, such as Bee-Bot®.
Whilst not a true Logo turtle, this can be given a sequence of move and
turn instructions, and even very young children quickly figure out for
themselves what it can, and cannot, do. More sophisticated floor turtles
can be found, such as Pro-Bot® and InO-Bot, both of which are 'proper'
turtles in the sense of being able to draw: the former can be programmed
using buttons on the device in a crude version of Logo, the latter on
screen using a building-block language inspired by Scratch. These
devices seem rather less popular than Bee-Bot® itself, perhaps because
of additional expense or because teachers think that when a pupil is
ready to move on from the Bee-Bot®, they're ready to move on to Scratch.

Scratch takes Logo turtles as a starting point, sprites in Scratch can
move and turn just as turtles do; they can also say things, play sounds,
change their appearance, interact with other sprites, respond to
external events and do lots of things that floor turtles can't. However,
in the current version of Scratch they can only draw using an additional
library of 'pen' commands, and they are confined to the world of the
screen.

Sooner, or hopefully later, the young programmer moves on from
block-based programming in Scratch or a similar environment, to
text-based programming, perhaps using a Logo interpreter here to help
bridge this gap, or perhaps jumping straight in to Python programming.
Even here though a good teacher might scaffold the transition to the
additional cognitive load of text-based programming through working in
the familiar territory of turtle graphics importing the necessary
methods from Python's Turtle module. This is a sophisticated toolkit,
and there are some lovely examples available, such as a playable, but
unbeatable, version of Nim, arguably the first ever computer game
(Flesch, 1951).

However, in all these instances, from toy robots through to programming
in Python, the child never *builds* a turtle: they just use one, either
on the floor or on screen, built by the experts. Back in 1971, I think
Papert and Solomon had in mind something a little more visceral. How
might we replicate this today?

## Physical computing

As well as the on-screen programming, many have argued for some sort of
physical computing to go with this: providing some introduction to input
and output beyond mouse, keyboard, and screen, touch or otherwise. LEGO®
Mindstorms® named after Papert's (1980) book, (Bumgardner, 2007),
offers one possibility here. Whilst the step-by-step build instructions
for a floor turtle are not included in the standard materials, a 'master
builder' would be able to figure these out for herself. For others,
Astolfo et al. (2007), provide an outline of what's
needed.

Another approach might be to make use of a micro:bit as the brains for a
floor turtle, using the edge connector to link this to a powered control
board for motors. There are kits to make something like this using a
micro:bit readily available. On the other hand, with a few bits of
hardware and some ingenuity, this approach comes close to Papert and
Solomon's idea of building ones own turtle.

## Processing

Another approach to making a turtle would be to reinterpret this as
making a *virtual* rather than physical turtle - adding at least some of
the turtle graphics commands to a language which doesn't have these
already, such as Processing.

Processing began back in 2001, thirty years on from Papert and Solomon's
paper, and took some inspiration from Logo, as a visually expressive
language, and one suitable as a first programming language. Processing
offers a way of using code to create beautiful visual and interactive
media, as well as modelling applications. Originally developed in Java,
it can usefully be seen as an introduction to programming in that
language, doing lots of the heavy lifting needed to get something
interesting up on screen whilst still scaffolding the syntax and
approaches. There's also a Python syntax version, but much of the most
recent development work has happened in the native Javascript version,
p5.js. For those working in schools this has the huge advantage of not
needing anything installed locally: there's an editor right there in the
browser, as well as the storage and persistent URLs needed for folks to
share their programs ('sketches' in the processing jargon) with a global
audience. One reason that Processing, particularly in its p5.js
incarnation works well as an introductory text-based language is that it
provides some immediate motivation for moving on from Scratch: it's hard
to persuade pupils who've created games, animations and music in Scratch
of the value to be found in searching through or sorting arbitrary lists
in Python, but much easier to convince them that it's worth learning the
syntax to create an amazing generative animation in p5.js.

Whilst Processing is designed with graphics in mind, out of the box it
has no implementation of Logo's turtle, but rather adopts an entirely
Cartesian model of the canvas: if you want to program a turtle in
Processing, you have to make one.

## Turtles as objects

To me, the most natural way to make a turtle in Processing is as an
object: the turtle has properties (its position on the screen, its
heading, whether the pen is up or down, perhaps the colour and thickness
of the line drawn), and methods (moving forward, backward, turning left
or right, picking the pen up, putting the pen down, heading home,
perhaps even reporting where it is and where it's headed).

The turtle then becomes not merely an object to think with for geometry,
but an introduction to object oriented programming, and a reference
object for thinking about some of these, often quite subtle, ideas.

Here's one attempt at defining a class of turtles, and constructing a
new object in the class, right at the centre of the canvas:
```js
    class Turtle {

    constructor(x_ = width / 2, 
                y_ = height / 2, 
                direction_ = -90, 
                penDown_ = true, 
                penColor_ = color(0)) {
        this.x = x_;
        this.y = y_;
        this.direction = direction_;
        this.penDown = penDown_;
        this.penColor = penColor_;
        }
    //...    
    }
```
We might then go ahead and start adding some methods, starting with
moving forward. As we're having to convert from the turtle-centric polar
frame to the canvas's Cartesian frame, the math here is high school, but
then so is object oriented, text-based programming.
```js
        forward(d) {
            let oldX = this.x;
            let oldY = this.y;
            this.x += d * cos(this.direction);
            this.y += d * sin(this.direction);
            if (this.penDown) {
                stroke(this.penColor);
                line(oldX, oldY, this.x, this.y);
            }
        }
```
Turning right and left though are just changes in the turtle's
direction:
```js
        right(a) {
            this.direction += a;
        }

        left(a) {
            this.direction -= a;
        }
```
Similarly, pen up and pen down instructions simply change the value of
the turtle's penDown parameter:
```js
        pendown() {
            this.penDown = True;
        }

        penup() {
            this.penDown = False;
        }
```
Once all the necessary methods have been created, it's time to put this
to the test. The code here, ran once as part of p5.js's setup procedure
draws a regular pentagon, as expected. You can see the code borrowed
from Logo and that from native Javascript:
```js
    function setup() {
      createCanvas(windowWidth, windowHeight);
      angleMode(DEGREES);
      background(220);
      ted = new Turtle();
      var i;
      for (i = 0; i < 5; i++) {
        ted.forward(200);
        ted.right(72);
      }
    }
```
More interesting examples might be experiments with Papert's notion of
the 'squiral' (Papert, 1980):
```js
    function setup() {
      createCanvas(windowWidth, windowHeight);
      angleMode(DEGREES);
      background(220);
      ted = new Turtle();
      var i;
      for (i = 0; i < 50; i++) {
        ted.forward(10*i);
        ted.right(74);
      }
    }
```
Which produces the following:

![petagonal squiral](/images/squiral.png)

Or, we can go further still, and implement recursion to create a
fractal, such as the Koch Flake (Koch, 1904).
```js
    function setup() {
      createCanvas(windowWidth, windowHeight);
      angleMode(DEGREES);
      background(220);
      ted = new Turtle();
      for (i=0; i<3; i++) {
        edge(400);
        ted.right(120);
      }
    }

    function edge(size) {
      if (size < 1) {
        ted.forward(size);
      } else {
        edge(size / 3);
        ted.left(60);
        edge(size / 3);
        ted.right(120);
        edge(size / 3);
        ted.left(60);
        edge(size / 3);
      }
    }
```
![Koch flake](/images/koch.png)

There is, of course, plenty more that can be done in turtle graphics,
and Processing itself. I have shared [my turtle class and an example
sketch](https://editor.p5js.org/mberry/sketches/XE-TOpv2) online for the reader to extend further.

<iframe src="https://editor.p5js.org/mberry/full/XE-TOpv2" width=600px height=600px></iframe>

What we have though is using Papert and Solomon's old idea of *making* a
turtle as a way in to understand some far deeper ideas than just
learning about exterior angles of polygons or making pretty patterns on
screen. *Making* a turtle crosses an abstraction boundary into hardware,
or at the very least, objects, properties and methods, all the while
staying within reach of the familiar home ground of the turtle itself.

>Originally published as Berry, M. (2021), Make a Turtle! in G Stager (ed.), *[Twenty Things to Do with a Computer Forward 50: Future Visions of Education Inspired by Seymour Papert and Cynthia Solomon's Seminal Work.](https://www.amazon.co.uk/Twenty-Things-Computer-Forward-Education/dp/1955604002)* Constructing Modern Knowledge Press, Torrance, CA, pp. 231-235.

# References

Astolfo, D., Ferrari, M. and Ferrari, G. (2007) *Building robots with LEGO mindstorms NXT*. Burlington MA: Syngress Publishing, Inc.

Boulay, B. du, O'Shea, T. and Monk, J. (1981) The black box inside the
glass box: Presenting computing concepts to novices. *International
Journal of man-machine studies*, 14 (3): 237-249.

Bumgardner, J. (2007) The origins of Mindstorms. *Wired*. Available at:
<https://www.wired.com/2007/03/the-origins-of-/>.

Flesch, R. (1951) *The art of clear thinking.* Harper.

Koch, H. (1904) Sur une courbe continue sans tangente, obtenue par une
construction géométrique <span class="nocase">é</span>lémentaire. *Arkiv
for Matematik, Astronomi och Fysik*, 1: 681-704.

Papert, S. (1980) *Mindstorms: Computers, children, and powerful ideas*.
New York, NY: Basic Books.

Papert, S., and Solomon, C. (1971) Twenty things to do
with a computer. *Cambridge, MA*.

