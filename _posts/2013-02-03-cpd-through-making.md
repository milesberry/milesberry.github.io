---
id: 863
title: CPD through making
date: 2013-02-03T20:12:10+00:00
author: Miles Berry
layout: post 
comments: true
guid: http://milesberry.net/?p=863
permalink: /2013/02/cpd-through-making/
categories:
  - CS
  - Teacher training
  - Uncategorized
---
I don’t think many would doubt that learning through making things, ideally for an audience of other people, is a highly effective way of learning in ICT (including CS) in schools. Papert made this case some time ago now. I rather think the same is true of many other subjects: art, music, D&T, English, history, geography, RE, although the ‘product’ and medium would need to fit the content. Similarly, [our experience at Roehampton](http://milesberry.net/2013/02/making-things-in-ict-at-roehampton/), and I’m sure that of teacher trainers elsewhere, suggests this is a highly effective approach to developing subject knowledge, subject pedagogy and curriculum knowledge in ICT (and I suspect other subjects too).

So. If learning though making is such an effective approach to ICT for initial teacher training and in schools, why not also for CPD? I know I’ve [blogged on this relatively recently](http://milesberry.net/2013/01/some-thoughts-on-cs-cpd/), but the idea continues to take shape. There are two sides to the CPD challenge:

  * mastering the subject content: to teach computer science it’s (almost) necessary to know that computer science;
  * developing the subject pedagogy: the Secretary of State complaining that many had told him that ICT was “[too off-putting, too demotivating, too dull](http://www.education.gov.uk/inthenews/speeches/a00201868/michael-gove-speech-at-the-bett-show-2012)”, wasn’t merely because of the subject content, but at least in part because of how some of us have taught it; I don’t doubt that we can teach Scratch just as badly as we’ve taught PowerPoint.

So, to tackle the first of these, I’m coming round to the position that the best approach is to get teachers coding, rather than merely teaching them about coding, but the learning is likely to be most meaningful if the stuff they’re coding is actually something they might use in their day jobs. What I have in mind, is a CPD programme that focusses on teachers working collaboratively to make interactive and online learning resources for their pupils. I know there are plenty of counter examples, and many of the commercial products are highly polished, but far too many of the curriculum resources bought by schools are suboptimal because they’ve been developed by folk who aren’t themselves teachers. So, two birds with one stone here: let’s get teachers coding, _and_ let’s get some lovingly crafted, pedagogically sound learning resources too.

The typical learning journey may not be that dissimilar from their students.

## A hands-on CPD programme for teachers {#ahands-oncpdprogrammeforteachers}

#### Scratch

Creating a few educational games and simulations in Scratch is really worthwhile and brings an easy win; I know there’d be some (probably more in the secondary phase) who’d see this as a bit of an insult to their intelligence, but Scratch’s ‘high ceiling’ philosophy, and the ease with which teachers can make interactive resources tailored for their own pupils and curriculum might win even these over.

#### HTML</p> 

Some web development work could provide a meaningful introduction to text based languages (and, yes, I know HTML isn’t a programming language, but Javascript is), as well as being highly amenable to learning through modding (qv [Hackasaurus X-Ray Goggles](http://hackasaurus.org/en-US/goggles/)). I’m very impressed by the beta version of [Decoded](http://decoded.co)’s new [web-development course for education](http://o2learn.decoded.co/html-css/lesson/0) for O2 Learn, and I use [Shay Howe’s Beginner’s Guide](http://learn.shayhowe.com/html-css/) with our 3rd Year trainees, both of which are fine as tutorial resources, but the main thing here is to get teachers coding something useful and, I think, working with the HTML itself, not in a WYSIWYG editor &#8211; remember the goal isn’t to make a webpage, but to develop an understanding of the web. Practical projects could be making presentations in one of the many lovely HTML5 presentation frameworks, eg [deck.js](http://imakewebthings.com/deck.js/), a few interactive teaching resources in [Undum](http://undum.com) and then perhaps some static site development linked directly to the curriculum using a framework like [Boilerplate](http://html5boilerplate.com) or [Bootstrap](http://twitter.github.com/bootstrap/).

#### LAMP

I’d probably stick with developing for the web for the next phase too, bringing in a server-side scripting language. I’m torn here between Python, which seems the language of choice for many in the CAS community, and PHP which is probably the quickest route into modding useful web-based apps on the LAMP stack. The usual open source favourites such as Moodle, WordPress and Drupal have open and well-documented architectures amenable to module hacking and development, with both Moodle and WordPress having a huge installed base in schools. The developer communities are pretty supportive too. Coding modules or plugins for these will also help / require teachers get to grips with the intricacies SQL databases.

#### Apps

After that, I think we’d be looking at some mobile app development. I think there’s an argument for the design led approach taken by CDI [Apps for Good](http://appsforgood.org) (and am now wondering if they do CPD courses for teachers), but that’s got to be alongside the programming work, which really needs to be the focus. Whilst the App Store and Play are crowded places, there are ways in for apps tailored to particular subject matter and school contexts. [App Inventor](http://appinventor.mit.edu/) is very nice, and really not _that_ much harder than Scratch. I’m told the learning curve for iOS development is fairly steep, but as with many of the above suggestions, a collaborative approach here is what’s needed, ideally with a few more experienced folk helping others along the way, as we see in, for example, [Young Rewired State](http://youngrewiredstate.org/). Whilst it’s not at scale yet, the teacher/developer pairing idea of [Computing++](http://www.computingplusplus.org/) makes sense, and I’d hope that some linkage between the BCS’s professional membership and CAS may yet emerge.

#### CS

Of course, the above approach focusses on the programming side of things, rather than the more theoretical computer science aspects. I’m confident that much of the theory can be learnt through a willingness to reflect on the experience of programming, but a little reading would, I’m sure help here. John Naughton’s [From Gutenberg to Zuckerberg](http://www.amazon.co.uk/Gutenberg-Zuckerberg-Really-About-Internet/dp/0857384252/ref=sr_1_1?s=books&ie=UTF8&qid=1359916262&sr=1-1) is highly readable and a good start on the Internet if not other aspects of computing. Whilst clearly created as a teaching resource, I’d have thought [CS Unplugged](http://csunplugged.org/sites/default/files/activity_pdfs_full/unpluggedTeachersMar2010-USletter.pdf) ideal for filling in much of the theoretical background, and this would naturally lead on to Paul Curzon’s as yet unpublished [Computing without Computers](http://www.eecs.qmul.ac.uk/~pc/research/education/puzzles/reading/). [Blown to Bits](http://www.bitsbook.com) is the set reading for Berkeley’s Beauty and Joy of Computing course. I’m enjoying Peter Bentley’s [Digitized:The Science of Computing](http://www.amazon.co.uk/Digitized-science-computers-shapes-world/dp/019969379X) at the moment, and this takes an unashamedly philosophical, whilst still highly accessible, stance.

Beyond these ‘introductory’ texts, there’s now any number of MOOCs on aspects of computer science, such as [Udacity’s CS101](https://www.udacity.com/course/cs101). I’ve been saying for a while now that we’re at the point where someone literate, connected and motivated can teach themselves most things, CS (if not dentistry) included. Motivation is the challenge, of course, but I’d hope that this is a box that those teaching ICT in primary and secondary schools could tick with confidence. What better way to model life-long learning. 

## Subject Pedagogy</p> 

Which brings me round nicely to developing subject pedagogy. The medium above, learning through making, is the message. It’s a commonplace that ‘we teach how we were taught’, and I live in hope that if teachers can learn programming through programming then there’s every chance that they may teach it that way. As well, though, as making learning resource, there’s plenty of other stuff (schemes of work, assessment frameworks, textbooks, VLE courses…)we’ll need to be making to get CS into schools and taught well, and again a collaborative effort here is likely to be powerful.

Ideally, I’d see this happening in local clusters, and crucially cross-phase; just the sort of thing which the remaining local authorities might facilitate. Primary and secondary teachers both have much to offer to this sort of collaborative effort: the former a long tradition of making teaching resources and learning through play, exploration and experiment which seems particularly appropriate, the latter more specialist subject knowledge and an understanding of what’s needed to get qualifications in the subject. Better still, would be to get university CS and education departments involved, alongside good folk from industries. Perhaps not the way we’ve done things in the past, but very in-tune with the sort of Big Society (OK, I know) approach which is characteristic of the move to more computing in schools.