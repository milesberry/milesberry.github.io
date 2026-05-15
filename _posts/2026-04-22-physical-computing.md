---       

layout: post       
title: "Physical Computing"       
date: "2026-04-22 18:00:00 +0000"
author: Miles Berry
permalink: /2026/04/physical-computing/
comments: true
image:
     feature: 260422.jpg
---

Physical computing has a long and distinguished history in UK computing education, stretching back to the BBC Micro of the early 1980s. That machine arrived in schools not through the Department of Education but through the DTI, which wanted every school in the country to have at least one computer. The BBC's branding gave the project a reach and legitimacy that a commercial product could not have achieved — a lesson that still resonates when we think about how the Raspberry Pi Foundation has shaped computing education not by getting its hardware into every classroom, but by ploughing the profits from hobbyist and industrial sales back into curriculum resources and teacher support.

The micro:bit is today's go-to platform for physical computing in schools, and for good reason. Its hardware is transparent in a way that most consumer electronics are not: the components on the back are labelled, the 5×5 LED matrix makes binary representation of data visible and immediate, and the edge connector along the bottom invites pupils to wire things up with crocodile clips and see what happens. Buttons, accelerometer, compass, microphone, Bluetooth Low Energy — all of it accessible through a few lines of code or a handful of blocks. It is hard to think of another piece of hardware that offers so much pedagogical surface area for the price.

The MakeCode editor, built on Google's Blockly toolkit, is the natural starting point for most school use. Its block-based interface will feel familiar to anyone who has taught with Scratch, and the on-screen emulator means pupils can write and test programmes without touching a physical device at all — a genuine advantage when you are managing thirty pupils and a box of micro:bits with mismatched USB cables. The emulator also makes it possible to introduce the programming ideas in a controlled session first, and then hand out the hardware as a payoff once the code is working. There is real value in that moment when something a pupil has written makes a physical object do something in the world.

That tangibility is the strongest argument for physical computing in the curriculum. When a pupil adjusts a variable and watches a light change colour or a buggy change speed, the relationship between code and effect is visible in a way it never quite is on screen. It also broadens the picture of what computing actually is. Programming is only part of the field: there are engineers who design the hardware, people who work on embedded systems and IoT, and a whole world of making that pupils may never encounter if their computing education consists entirely of sorting algorithms and Scratch animations. Physical computing opens a door to that wider world.

Good starting projects for the micro:bit include a binary counter triggered by button presses, a rock-paper-scissors game using the shake event, a ball-in-the-hole tilt game using the built-in sprite library, and a virtual pet. More ambitious possibilities include using Bluetooth radio to model the spread of a pandemic across a room full of devices, or using the micro:bit as a physical controller for a Scratch game. Each of these connects naturally to curriculum content: binary representation, selection, iteration, variables, events, randomness — the micro:bit covers a lot of ground.

There are honest implementation challenges worth acknowledging. Physical hardware takes time to manage, and that time comes out of the learning. The question of whether to use the emulator, the physical device, or both is worth thinking through before the lesson rather than during it. It is also worth knowing where physical computing sits in your school's scheme of work — and how much room you have to design your own tasks. Not every department will give trainees the freedom to run open-ended making projects; in many schools the scheme of work is fixed and the job is to teach it well. Both approaches have merit, and knowing which one your school expects is important.

The micro:bit also connects to some of the bigger curriculum topics. The 5×5 LED grid is a natural demonstration of binary representation. The device abstraction layer in MicroPython is abstraction made concrete. And as the new GCSE Computing specification takes shape — with data literacy and AI expected to feature alongside algorithms and programming — the micro:bit's sensor array and Bluetooth radio suggest all sorts of possibilities for data collection and machine learning projects that are still to come.

*Based on the 18th Roehampton Computing Education lecture, Physical Computing, 22 April 2026*