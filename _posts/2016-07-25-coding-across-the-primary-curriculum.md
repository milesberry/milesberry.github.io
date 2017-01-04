---
id: 1400
title: Coding across the primary curriculum
date: 2016-07-25T17:21:39+00:00
author: Miles Berry
layout: post
guid: http://milesberry.net/?p=1400
permalink: /2016/07/coding-across-the-primary-curriculum/
categories:
  - Uncategorized
---
Quite recently, we thought the future of ICT education would be one in which technology was embedded seamlessly throughout all aspects of teaching and learning, and that all a child could possibly need to learn about IT could be taught within the context of other subject areas. The seamless embedding of technology throughout the life of a school remains a dream for many, but schools at the cutting edge have already achieved much with 1:1 devices, robust wifi, great training and a vision for how technology can transform education.

On the other hand, few would now argue that we can teach the new computing curriculum without setting aside some dedicated time to mastering the content of this new foundation subject. In the move from ICT to computing, our focus shifted away from the skills of using technology to knowledge and understanding of the principles of information and computation. It seems that mastering the foundational ideas of computer science, and particularly programming, requires some dedicated curriculum time. That’s not to say though that computing should be taught in isolation: the other subjects can provide motivating, relevant contexts for pupils to apply their computational thinking and programming skills.

## Computational thinking

 [Computational thinking](http://milesberry.net/2014/03/computational-thinking-in-primary-schools/) is the golden thread running through the computing curriculum: this is about looking at problems in such a way that a computer can help us solve them. It draws together such concepts as logical reasoning, decomposition, patterns, abstraction and algorithms, as well as approaches such as tinkering, making, debugging, persevering and collaborating.

The foundations of computational thinking are laid in EYFS’s [characteristics of effective learning](http://www.foundationyears.org.uk/files/2012/03/Development-Matters-FINAL-PRINT-AMENDED.pdf), but these concepts and approaches can be applied to any area of the primary curriculum further up the school: following or writing instructions makes use of algorithmic thinking; doing corrections in maths is debugging; looking for explanations in science is logical reasoning, and so on. As pupils become better at computational thinking through computing lessons, they’ll be better able to apply this across the curriculum.

I think we can go further than this though. As pupils have been getting better at programming, I think we’re reaching the point where they can start to use this to do some creative things in other subjects. This isn’t merely about using other subjects as a context for learning to code, this is about coding as a way to help pupils learn in other subjects too. Here are some examples:

## Maths

The relationship between maths and programming goes back to Alan Turing and the the foundations of computer science. Simple turtle graphics are a great way to help pupils get a far more visceral feel for geometry, as they put themselves in the place of the turtle. Pupils quickly learn for themselves that exterior angles sum to 360˚. Writing programs where sprites move around the screen in Scratch similarly makes coordinates and negative numbers seem more real and more useful.

<figure>
<img src="/wp-content/uploads/2016/07/download.png">
<figcaption>Snap! code for finding highest common factors using Euclid&#8217;s algorithm
</figcaption>
</figure>



In maths, we make use of algorithms (sequences of steps and sets of rules) all the time. We’ll teach pupils algorithms for checking if a number is prime, for finding common factors or for doing arithmetic with fractions. With a few coding skills, pupils could put their knowledge of these to the test by writing their own programs to implement these rules, trying them out with much bigger numbers than the exercises we set, and perhaps even finding faster algorithms for the same problem.

## Music

Scratch has music making tools built in &#8211; it’s easy enough to record and play back audio, but it’s well worth getting pupils to experiment with creating music by sequencing notes and their durations. There’s a range of instrument and percussion available, and it’s possible to play multiple notes at the same time, so pupils can experiment with chords and polyphony. Repetition in programming can be linked to music compositions too, and pupils can explore randomly generated music, or music that reacts to input from mouse, keyboard or sensors. Pupils can improve their compositions in the same way as they debug their programs.

Beyond Scratch, [Sonic Pi](http://sonic-pi.net/) and [EarSketch](https://earsketch.gatech.edu/landing/) take the text-based, grown-up programming languages Ruby and Python and make them directly applicable to musical composition. They’re certainly accessible to upper primary pupils, but go way beyond that level. There’s some amazing work going on at the moment at the intersection between music and computer science.


```ruby
use_bpm 90
use_synth :pretty_bell

define :sequence1 do
play_pattern_timed [:e,:e,:f,:g], [0.5,0.5,0.5,0.5]
play_pattern_timed [:g,:f,:e,:d], [0.5,0.5,0.5,0.5]
play_pattern_timed [:c,:c,:d,:e], [0.5,0.5,0.5,0.5]
end

sequence1
play_pattern_timed [:e,:d,:d], [0.75,0.25,1]
sequence1
play_pattern_timed [:d,:c,:c], [0.75,0.25,1]
play_pattern_timed [:d,:d,:e,:c], [0.5,0.5,0.5,0.5]
play_pattern_timed [:d,:e,:f,:e,:c], [0.5,0.25,0.25,0.5,0.5]
play_pattern_timed [:d,:e,:f,:e,:d], [0.5,0.25,0.25,0.5,0.5]
play_pattern_timed [:c,:d,:g3], [0.5,0.25,1]
sequence1
play_pattern_timed [:d,:c,:c], [0.75,0.25,1]
```




## D&T

There’s an expectation in [the Design and Technology curriculum](https://www.gov.uk/government/publications/national-curriculum-in-england-design-and-technology-programmes-of-study/national-curriculum-in-england-design-and-technology-programmes-of-study#key-stage-2) that pupils at Key Stage 2 will

> “apply their understanding of computing to program, monitor and control their products.”

Platforms such as the Lego WeDo, Crumble and the BBC micro:bit make it much easier than ever before for pupils to take their first steps into the realm of ‘physical computing’, using buttons, switches and sensors to accept input, writing their own code to process this and producing output through LEDs, speakers and motors. Whilst the BBC micro:bit’s initial distribution was to secondary schools, the online editor and emulator is accessible to all at [microbit.co.uk](http://microbit.co.uk).

The most exciting work in physical computing, at school and beyond, is happening on the [Raspberry Pi](https://www.raspberrypi.org/): which has a set of general purpose input and output pins built in, and support for using these from its own version of Scratch. There’s a ‘sense hat’ too, which incorporates a tiny display, joystick and some sensors: a couple of these, with programs written by British school children, went up to the international space station with Tim Peake for the [Astro Pi](https://astro-pi.org/).

## Art

Turtle graphics in Scratch, Logo or Python needn’t be restricted to maths &#8211; there’s ample scope to use this as a medium for pupils creative work in art too. QCA’s [old scheme of work for ICT](http://webarchive.nationalarchives.gov.uk/content/20090608182316/http://standards.dfes.gov.uk/schemes2/it/itx4b/?view=get) had a lovely unit on crystal flowers, there’s plenty of scope to explore tessellating patterns and Islamic art has a rich history of beautiful, geometric art to provide inspiration here. There’s also scope for exploring more natural patterns, experimenting with simple code to create recursive fractals for trees, fern leaves, broccoli or coastlines.

<div id="attachment_1402" style="width: 310px" class="wp-caption aligncenter">
  <img class="wp-image-1402 size-medium" src="http://milesberry.net/wp-content/uploads/2016/07/Screen-Shot-2016-05-14-at-18.39.42-300x281.png" alt="Fractal broccoli in Scratch" width="300" height="281" srcset="http://milesberry.net/wp-content/uploads/2016/07/Screen-Shot-2016-05-14-at-18.39.42-300x281.png 300w, http://milesberry.net/wp-content/uploads/2016/07/Screen-Shot-2016-05-14-at-18.39.42.png 798w" sizes="(max-width: 300px) 100vw, 300px" />

  <p class="wp-caption-text">
    Fractal broccoli in Scratch
  </p>
</div>

## Foreign languages

Scratch has excellent support for working in foreign languages &#8211; the familiar English of the programming blocks can be replaced with keywords from many other languages, even including Latin. This is great for pupils learning English as an additional language, but is also a nice way to build up pupils’ familiarity with a foreign language. Scratch is great for producing short, scripted animations, with on-screen and recorded dialogue or narration: why not have pupils program animations for a language they’re learning, or even a simple chatbot?

<div id="attachment_1403" style="width: 310px" class="wp-caption aligncenter">
  <img class="wp-image-1403 size-medium" src="http://milesberry.net/wp-content/uploads/2016/07/Screen-Shot-2016-05-14-at-20.48.48-300x290.png" alt="Coding is the new Latin!" width="300" height="290" srcset="http://milesberry.net/wp-content/uploads/2016/07/Screen-Shot-2016-05-14-at-20.48.48-300x290.png 300w, http://milesberry.net/wp-content/uploads/2016/07/Screen-Shot-2016-05-14-at-20.48.48.png 756w" sizes="(max-width: 300px) 100vw, 300px" />

  <p class="wp-caption-text">
    Coding is the new Latin!
  </p>
</div>

You can also program Scratch (or Python) to generate semi-random, but grammatically correct sentences, using the computer science idea of a finite state machine. Playing with this gives some insights into the structure of a language: you could do this for English, but also for any other language that pupils are learning.

&nbsp;

Looking for ways for pupils to use their IT skills across the curriculum, such as searching for information, making presentations and editing videos, remains as valuable as ever. Alongside this, I think we should now start looking for some of the cross-curricular ways that pupils can use their programming skills too.

<p style="padding-left: 30px;">
  <em>Originally published in <a href="http://www.teachwire.net/" target="_blank">Teach Primary</a>, June 2016. © all rights reserved. I explored these ideas further, with reference to the secondary curriculum, in my plenary at #casconf16:</em>
</p>

<iframe width="640" height="360" src="https://www.youtube.com/embed/-JBgaR8sNcE" frameborder="0" allowfullscreen></iframe>
