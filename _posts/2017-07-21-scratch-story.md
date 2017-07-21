---
layout: post
title: "A Scratch Story"
date: "2017-07-21 10:00:56 +0000"
author: Miles Berry
permalink: /2017/07/scratch-story/
comments: true
---

I started playing with Scratch when I was a head teacher, back in 2009. I did my bit in the school's extracurricular programme, running a computer club - we had a Ubuntu thin client network, and I thought we might introduce the club to Squeak E-Toys, but then heard about Scratch. It looked good and we could run it under Ubuntu.

We did the fish tank animation thing (I take some credit for popularising this in the UK via the big BETT TeachMeet the following year), wrote a maze game and duck shoot game, and then wanted to try a driving game, with the idea of the player racing against the computer. This, for me, back then, was harder than it sounds. The algorithm was simple:

    keep driving forward,
    if you leave the track to the left,
         turn right,
    if you leave the track to the right,
         turn left.

The trouble was getting the car sprite to detect which direction it had left the track - after a some tinkering, I settled on using coloured 'sensors' as part of the car's costume and then using the < colour [] is touching [] > sensing block to take control.

It's a program that's stayed with me over the intervening eight years. Firstly, if you introduce a variable speed for the car, it's a great way to illustrate most of the programming constructs we now cover in the English computing curriculum for 7-11 year olds:

>use sequence, selection, and repetition in programs; work with variables and various forms of input and output
> use logical reasoning to explain how some simple algorithms work and to detect and correct errors in algorithms and programs

There's a version of this in [a programme I made with Glasshead for the BBC](http://www.bbc.co.uk/programmes/p016j4g5), which shows an interesting 'bug' in the code - if you set the speed too high, the car appears to veer of the track. For most pupils, it's not immediately apparent what causes this, and indeed one could argue that it's simply a realistic simulation, with an important Driver Education message - drive too quickly, and you will lose control!

When I was writing Switched On Computing, I included [this program](https://scratch.mit.edu/projects/11932304/) as a basis for a debugging activity. As a result, it's one of my more popular Scratch programs, with close on 25,000 views and some 690 variants in its remix tree - one of the many, many things I love about Scratch! There are some really creative solutions to the challenge, as well as some fun variations, in the tree. There's also some amusing feedback, for example, the first comment I got on this:

>How many SCRATCHES have you done before? I hope it is slightly better when it is finished.

I coped. I have broad shoulders, and 'Primaryicttech' valiantly leapt to my defence:

>This is a script written by a Computing expert for children to learn from by debugging. The author has done many Scratch projects before and has set this one up as a learning exercise.

It's still a program I talk about when presenting. These days, I mention it when talking about the insights coding offers to the other subjects we teach, and we segue neatly on from simple turn left / turn right rules to the rules of the road, and the ethical rules we'd want self-driving cars to follow: deep in the programming of which must be something similar to my algorithm above.
