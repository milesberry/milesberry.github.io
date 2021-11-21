---
layout: post
title: "Principles of practical programming"
date: "2021-11-21 12:30:56 +0000"
author: Miles Berry
permalink: /2021/11/practical-programming/
comments: true
image:
        feature: 211121.jpg
---

The suggestions here are offered as pragmatic advice on what good practical programming work for a secondary class might look like. Not all of these principles or characteristics will apply all of the time in every programming class. I write here about using programs to solve problems, but this should be interpreted to also include developing open ended, creative projects or creating a program which fulfils the requirements of a given design brief.

## Keep the big picture in mind, and focus on the details.

Programmers typically work at two levels of abstraction at the same time, which is one of the reasons why this is so hard for many novices. Teachers can help pupils manage these demands by suggesting strategies for keeping track of the big picture (e.g. clear statements of the problem, example results with test data, outline flowcharts), whilst also focussing on the detail of particular code block or statement. Over time, and repeated practice, some of the detail will become automatic, or nearly automatic, but teachers can help here by supporting the mental 'chunking' of common syntax, constructs and patterns.

## Reading comes before writing

Pupils should have ample opportunity to read programs written by others, including those in textbooks, in online sources, written by their teachers and by their peers. Where they are provided with high quality example code, they should be able to explain what the program, blocks of code and individual lines of code do. They should be able to run the program by hand, or in their head, predicting its output. Where the examples are lower quality, they should be able to critque these, suggesting improvements, correcting bugs or refactoring functions to improve efficiency or reliability.

## Thinking comes before coding

Before pupils start coding, they should have a clear idea of what their program will do and how it will work. For complex problems, encourage them to make notes on this, perhaps as loose pseudocode or as an outline flowchart; for simpler programs, some pupils may be able to retain their plan in working memory, but check that they can articulate how they intend to solve the problem. The 'computational thinking' concepts of logical reasoning, algorithms, decomposition, abstraction and pattern recognition are particularly important at this stage of the process, and many teachers find it helpful to discuss these explicitly when helping pupils plan their programs.

## Show how you would do it

Working through example problems and projects with a class can be effective in teaching the strategies and tactics of practical programming. Writing a program live in front of the class models the thought processes of the programmer far more effectively than presenting a complete solution for pupils to study. It is important to explain what you are doing at the time, drawing pupils' attention to both the overall approach to tackling the problem or project as well as the detail of implementation. This can be particularly effective when done interactively with the class, asking pupils to offer suggestions, explanations or predictions, as well as asking them to spot any mistakes you make. Also model how you go about fixing any bugs in the code.

## Use common patterns

Pupils should come to recognise common solutions to common problems. These can be taught explicitly, but pupils should also have repeated experience of implementing standard design patterns, algorithms and data structures in their own code. Standard data structures such as lists or two dimensional arrays will be used for solving many different problems. For many problems at GCSE and beyond, pupils will need to update an accumulator variable over a list if elements meet a condition. Efficient algorithms for search and sort can be applied in multiple contexts, and many games or interactive simulations make use of the model-view-controller design patter.

## Use a modular approach

Show pupils what a modular, well-structured program looks like and expect them to develop modular solutions themselves. Explain the benefits of creating re-usable functions, and make sure pupils make use of this approach to manage the complexity of developing their own programs. Ask pupils to decompose their solution to a problem into its components and consider how these components can be implemented as distinct functions in their program. Pupils can then write code for these functions, testing each as they go. They can subsequently improve these if they wish, once their code is working.

## Develop a positive attitude to debugging

Pupils' programs will rarely work first time, and it is unhelpful for teachers simply to correct pupils' code for them. Rather, the emphasis should be on using mistakes as an opportunity for learning. Pupils can be provided with buggy code and asked to find and correct all the mistakes present. At the syntax level, debugging affords useful re-enforcement of the requirements of the programming language, and pupils will soon come to remember these with a degree of automaticity. Semantic or logical bugs are harder to spot, and pupils should be taught methods for finding these for themselves, such as adding print statements to check intermediate values, working through the program by hand using a trace table, and paying attention to the end conditions of loops and the edge conditions of tests. Provide general guidance on how to debug a program, and encourage pupils to reflect on how the bug arose and what they had to do to correct it.

## Check your work

Pupils should check through their programs as they write them. *Before* they run their code, ask pupils to look through and correct all the mistakes they can. Are they confident that the program will run and produce the answer they expect? Encourage pupils to develop and use test data, making sure that the program functions as it should for input data, for edge cases and fails safely and courteously when presented with invalid input. Ask pupils to test as they code, making sure that each function they write performs as it should. Over time, introduce pupils to the idea of test driven development, where the automated testing is created before the program, which clarifies its specification and helps assure its correctness.  

## Expect explanations

Pupils should be able to explain not just what their program does but also how it does it. Just as they should be able to read someone else's code and explain how it works at program, block and statement level, they should be able to do this for any code they write themselves. Ask them to add comments to their code to explain how the program works. It can be helpful to write these comments *first* before coding, establishing clear, labelled sub-goals for the work to come and making explicit how they decomposed their problem into sub-problems. Introduce pupils to [*literate* programming](https://en.wikipedia.org/wiki/Literate_programming), where they explicitly document their 'working out' for the reader, narrating the processes through which their program was developed. Pupils might experiment with making screen recordings of their coding, narrating their thinking as they develop their programs.

## Encourage collaboration

Pair programming is an effective and efficient software development strategy in which programs are written by two developers working side by side, sharing the keyboard, mouse and screen, typically with one taking on a driver-like role with the other acting as navigator. Many teachers report success with this approach in the classroom too. In class, pair programming needs careful management, as the focus must move from producing working code to making sure that each partner learns the underpinning constructs and approaches. Collaboration need not be limited to an individual partner: working as a member of a larger team introduces pupils to the demands and responsibilities of teamwork, and the benefits of good documentation, testing and modular code.

## Find meaningful contexts

Some argue that many pupils lose interest in computer science because the contexts of their programming in secondary school seem far removed from their interests and experience. The deregulation of practical programming at GCSE provides an excellent opportunity to adopt a more learner-centred approach to practical work, basing tasks on areas of genuine interest or concern to pupils. The appendix makes a number of suggestions here, but code can be used as the medium for creative work in interactive fiction, photography and other visual arts, musical composition and animation, as well as a means to visualise and find patterns in data from live and historical sources. Without the demands of a formal non-exam assessment, pupils can pursue their own individual programming projects.

## Encourage independent learning

Pupils' independent project work offers an opportunity for independent, self-directed learning. Be explicit in suggesting strategies for how pupils might teach themselves new concepts and techniques relevant to the difficulties they encounter when working on their own projects. Suggest reliable sources for independent study, including text books, language documentation, online materials such as [Isaac Computer Science](https://isaaccomputerscience.org/) and [Runestone Interactive](https://runestone.academy/) and communities such as StackOverflow. Be clear that it's not enough to copy and paste code from elsewhere, even if the source is acknowledged: what matters is pupils' learning how the code works and how they could apply the approach they've learnt to other problems. A regular homework in which pupils continue to work on an extended project, and pursue their own independent study to support them in doing so, can be of value, although teachers would be wise to expect regular updates on progress.

## Offer experience of multiple development approaches

As pupils move from coding simple programs to developing more complex projects, it is useful for them to learn about some of ways in which software engineers manage such projects. Pupils should learn about the traditional 'waterfall' approach, which proceeds from requirements through specification to code, testing and maintenance. They should also learn about iterative development, in which working code is successively improved through the implementation and integration of new features or gains in efficiency or reliability through rewriting the code for parts of the program. Pupils might also benefit from exposure to some of the ideas of agile development, such as pair programming, test-driven development, time-boxed development sprints and peer code reviews.

## Aim for fluency

The aim should be for pupils to achieve some degree of fluency in a high level programming language, so that they can move beyond learning the language to being able to use this to solve computational problems and express their own creative approaches. Whilst this may sound daunting, once pupils have understood how a particular language handles input, output, variables (and other data structures), selection, repetition and modularity, any problem that *can* be solved by a computer is, at least in theory, open to them.  It's useful to concentrate, perhaps exclusively, on just one programming language, using it repeatedly until its syntax and keywords become automatic. This sort of fluency in a language is developed through deliberate practice, beginning initially with simple, problem solving exercises or modifying existing code, but directing pupils attention to the act of *learning to program*, not merely to programming itself. There is no need for pupils to be constrained by the sort of programming required in the written exam papers, and many will relish making use of the expressive power of language and available extensions to it. Encourage pupils to follow the standard conventions of the language, such as widely accepted 'Pythonic' ways to do things and the [PEP8 style guide for Python](https://www.python.org/dev/peps/pep-0008/). Pupils should also become skilled at using a particular text editor or integrated development environment, making use of its core features and keyboard shortcuts without much conscious thought, so that their working memory can be applied to learning to program.