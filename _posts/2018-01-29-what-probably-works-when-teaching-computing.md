---
layout: post
title: "What probably works when teaching computing"
date: "2018-01-29 10:00:56 +0000"
author: Miles Berry
permalink: /2018/01/what-probably-works-when-teaching-computing/
comments: true
image:
        feature: 180129.jpg
---

Computing is a relatively new subject on the English national curriculum and at GCSE, so there's not yet the body of practice, and research evidence, for what makes teaching the subject particularly effective. It's fair to assume that most of what we know about good teaching across the curriculum applies in computing just as much as in any subject: providing clear explanations of new ideas, giving pupils the opportunity to practice applying new knowledge, and helping pupils integrate new concepts into the existing mental schemata all seem just as relevant to computing as to any other subject.

That said, computing has some distinctive characteristics, which ought to be taken into account. For example, in programming pupils can get immediate feedback from the compiler or interpreter they're using about whether their program *works*: they don't need a teacher to tell them if there's a spelling or grammar mistake in their code, and, most of the time, they can tell whether their program produces the output it should. Tightening up the feedback cycle, and removing the fear of 'getting things wrong' ought to help pupils learning to code, and those who teach them. On the other hand, pupils embarking on a GCSE in computer science are likely to have far less prior experience of the subject than those at the start of, say, GCSE physics, who'll have played with springs, magnets and circuits when they were back at primary school: it'll be some time before the curriculum changes provide a similar background of prior learning for CS students, and thus its perhaps not surprising that GCSE results are, for now, often lower than in other academic subjects.

We do have *some* evidence to draw on when trying to work out what is most likely to work when teaching computing. Back in the 70s and 80s Seymour Papert and his followers introduced Logo programming in the classroom, initially with robots (floor turtles) and then with equivalent turtle graphics on screen: Papert's own account of this work in his 1980 book, *Mindstorms: Children, Computers and Powerful Ideas*, still provides an inspiring view of how children can learn big ideas through playful and creative programming, even if quantitative data about the impact of this approach is largely absent. There's also a substantial body of research into what's effective when teaching programming, and other elements of computer science, to undergraduate students - whilst this is a rather different population to pupils in upper secondary education much of this research does seem relevant, and provides at least a starting point for developing our subject-specific pedagogy in school.

There are some things which have already become part of the 'lore' of computing teaching for which we've little evidence. For example, there's a view that the 'computational thinking', necessary for using or programming computers to solve problems, applies across and beyond the curriculum - that somehow pupils who've learnt logical reasoning, algorithms, abstraction and generalisation in computing will apply these to the other things they study, and to the problems they encounter in everyday life: there's not been any study since Jeanette Wing introduced computational thinking in 2006 that has successfully demonstrated that students in a CS class transferred knowledge from that class into their daily lives[^guzdial].

Similarly, the view that pupils will just pick up coding for themselves through play and experiment seems rather misguided - studies of independent programming even in an accessible language such as Scratch suggest many problems with the code produced and hint at some significant misconceptions. Unplugged approaches to teaching computing have grown in popularity, but at least one comparative study suggests that these have actually resulted in pupils being less interested in pursuing CS further compared to more traditional, hands-on approaches. Again, as far back as 1977, studies revealed no significant difference in success on programming tasks for students who'd been taught flowcharting and those who hadn't, and yet this approach to algorithm design and representation remains popular at GCSE: real coders don't draw flowcharts.

[^guzdial]: Guzdial, M., 2015. Learner-centered design of computing education: Research on computing for everyone. Morgan & Claypool Publishers.

So, what does work?

Firstly, I think we need to be honest about computational thinking. We should see this as

> the thought processes involved in formulating a problem and expressing its solution(s) in such a way that a computer ... can effectively carry out. [^wing]

The key thing here is that computational thinking should lead to computation - it's not some vague problem solving toolkit, but it is, I think, the essential planning needed when we're using computers to help us solve problems. Unlike mathematical reasoning, computational thinking is less concerned about getting an answer than establishing an automatable method to get an answer, to the specific problem and problems like it.

Computational thinking of this nature is something that has to be taught - you can't expect pupils to think computationally simply through exposure to programming. When NFER evaluated the impact of Code Club[^NFER], they found that, whilst Code Club attendees had got significant better at coding than their peers, they'd not made significantly better progress in computational thinking: if you want pupils to get good at thinking computationally, you have to teach them to do so.

[^wing]: Wing, J, 2014. Computational thinking benefits society. Social issues in computing, available at [http://socialissues.cs.toronto.edu/index.html%3Fp=279.html](http://socialissues.cs.toronto.edu/index.html%3Fp=279.html)
[^NFER]: Straw, S, Bamford, S and Styles, B, 2017. Randomised controlled trial and process evaluation of code clubs. Slough: NFER.

One way of developing computational thinking, and of helping pupils with programming, is through subgoal labelling. Whilst this approach isn't unique to computing, it does work really well in this context, and isn't that far removed from how professionals go about software projects. With subgoal labelling, the teacher (and later the learners themselves) identify the subgoals which need to be achieved in order that the overall goal be accomplished, labelling these explicitly. Over time, pupils will come to recognise that similar subgoals are needed in many different programming projects, and become adept at writing the code to accomplish these. In practical terms, this can be as simple as writing the comments for a program *before* writing the program itself.

One of the challenges computing teachers face is helping pupils construct a mental model of how a particular compiler or interpreter will run their code - in other words providing a 'notional machine' on which the programmer might imagine their program being run, and thus be able to predict confidently what their code will do. Many of the misconceptions that pupils have about programming stem from an inaccurate or unhelpful mental model of how computers work: for example that variables are like shoeboxes or that the computer will be able to guess what a particular bit of code was meant to do. It's worth being explicit about how a computer, and the programming language used, actually works, and taking care when resorting to real-world analogies of computational processes.

If pupils do have a good mental model of how a computer, and the language, works, they should be able to apply logical reasoning to code tracing exercises: given some code, can they predict what the program will output? Can they spot in advance logical bugs in the code they're given? Can they write down the value of variables in the program (particularly in loops) at each step as their code runs? Doing this away from the computer itself is fine. Indeed, it's a great idea to get pupils reading code before they start writing code. In English, we wouldn't dream of teaching pupils to write before they've learnt to read: the same applies to programming - reading, and stepping through, good example code may well be the best way to learn to write, and debug, code.

Whilst collaboration seems to be discouraged when it comes to exams and the NEA, it's commonplace in real world software development. It also seems to be effective way for learning to program. Pair programming started life in the world of agile software development, with two programmers working together on the same program, sharing the computer between them. Typically one programmer will take the 'driving seat', whilst the other's role is closer to that of navigator. This can work well in the classroom too, as long as the focus is kept on learning to program, not on merely getting code that works, and both pupils accept the shared responsibility for this.

There's much else that those teaching in school can learn from the research into effective computer science teaching at university level, and I think it's well worth teachers engaging with this work. As computer science becomes better established at school level, I think there's also the opportunity for teachers to add something to the knowledge of what (probably) works: if you're trying something new with your class, think of ways of testing whether the intervention actually is effective, and look for opportunities to share these insights with the rest of our community.

*Originally published in PiXL's Computing conference programme.*