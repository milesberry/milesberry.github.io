---
id: 844
title: Adaptive Learning and Interactive Fiction
date: 2013-01-18T21:09:56+00:00
author: Miles Berry
layout: post
guid: http://milesberry.net/?p=844
permalink: /2013/01/adaptive-learning-and-interactive-fiction/
categories:
  - CS
  - Ed Tech
  - Uncategorized
---
_A post prompted by a discussion on the Mirandanet discussion list asking for software suggestions for developing adaptive learning materials._

I&#8217;m still not _quite_ sure how I feel about adaptive learning, and I think this is down to some concerns about the &#8216;computer knows best&#8217; which can be detected beneath the surface. My first encounter was a rather lovely &#8216;teach yourself trigonomety&#8217; text (probably [Austwick&#8217;s Trigonometry: the right angled triangle](http://www.worldcat.org/title/trigonometry-the-right-angled-triangle/oclc/30293229)) that I checked out from our local library at a very young age &#8211; pages comprised trig problems with multi-choice answers, you followed the page reference for what you thought was right and then got specific feedback or another, slightly harder problem. Cool stuff, back then, and reminiscent of Ian Livingstone&#8217;s [Fighting Fantasy](http://fightingfantasy.com) game books, of which I played a few not longer after.

As Roger Broadie pointed out on the Mirandanet list, adaptive learning design seemed pretty cool back in the mid 2000s when we were all excited about VLEs and learning objects. Ruth Kelly summed the vision up well in the introduction to the [e-strategy](https://www.education.gov.uk/publications/eOrderingDownload/1296-2005PDF-EN-01.pdf):

> In the future it will be more than simply a storage place – a digital space that is personalised, that remembers what the learner is interested in and suggests relevant websites, or alerts them to courses and learning opportunities that fit their needs.

These ideas are, perhaps, due for something of a renaissance, with current interest in learning analytics, which I see as essentially the application of the data mining techniques of credit/loyalty cards to the massive data sets that could be generated as more and more of a pupils&#8217; work and interaction with the education system moves online. A sat-nav approach to the learning journey if you will &#8211; ie a system that has a pretty accurate picture of where the learner is (their profile), a map of the landscape (curriculum?) and some way of establishing the most efficient route to the destination (ideally crowd-sourced), chosen, on a good day, by the learner themselves. All well and a good way of getting from A to B.

Perhaps, though, there&#8217;s more to learning than getting to a destination; perhaps education ought to be a bit more about exploring a landscape, and a bit less about completing a journey? Google and Wikipedia are _different_: The former has a pretty good model of what I&#8217;m interested in (qv [Pariser on the Filter Bubble](http://www.thefilterbubble.com)) and is startlingly effective at finding the right content (learning object?), the latter, thanks to the network of links, a wonderful place to explore and discover things that I _wasn&#8217;t_ interested in. There are parallels here between downloading the e-text you want from the Web and browsing books and journals in a good library: the former is certainly more efficient, but the latter allows much more opportunity for chance discoveries.

Playing with adaptive learning in the VLE isn&#8217;t too hard &#8211; Moodle&#8217;s [Lesson module](http://docs.moodle.org/24/en/Lesson_module) has plenty of flexibility, and at a higher level Moodle 2 has support for [conditional activities](http://docs.moodle.org/22/en/Conditional_activities). [LAMS](http://www.lamsfoundation.org/index.htm) is still around, and there are polished, commercial tools like [Articulate Storyline](http://www.articulate.com/products/storyline-top-features.php#interactivity_href) for developing e-learning materials.

One of the early lectures in the Roehampton Creativity and Computing module looks at non-linear narrative, which gives students a great excuse to check out the aforementioned Fighting Fantasy game books from the library, play old school text adventures (eg [Zork](http://thcnet.net/error/index.php)), watch a little of [Get Lamp](http://www.getlamp.com) and learn a little about [Kristian Still](http://www.kristianstill.co.uk/wordpress/)&#8216;s impressive work using IF (interactive fiction) at the intersection of literacy and coding.

Now there&#8217;s a thought&#8230; Surely it wouldn&#8217;t be too difficult to take some of the tools used for developing Interactive Fiction, like [Inform7](http://inform7.com) or [Quest](http://www.textadventures.co.uk/quest/) and use these to knock up some quite complex adaptive learning tools. The tool that&#8217;s really caught my attention though is [Undum](http://undum.com), which is a lovely HTML5 / Javascript client side framework for interactive fiction &#8211; check out the [tutorial](http://undum.com/games/tutorial.en.html) and the [Mark of the Ninja](http://www.markoftheninja.com/undum/) to get a feel for this. Like [HTML5 presentations](http://imakewebthings.com/deck.js/) and [Bootstrap](http://twitter.github.com/bootstrap/), another example of how learning a little HTML (and a bit of Javascript this time) opens up some powerful possibilities for teachers to build high class teaching resources themselves.

Of course, as [Papert argued back in 1971](http://dspace.mit.edu/handle/1721.1/5835) in relation to drill and practice programs that children learn much more through making educational software than through using educational software:

> It is said that the best way to learn something is to teach it. Perhaps writing a teaching program is better still in its insistence on forcing one to consider all possible misunderstandings and mistakes.

I could see a far stronger case for getting students to code up some adaptive learning resources, perhaps using IF tools, than using AL resources. I&#8217;m thinking now about where I might be able to squeeze this sort of thing in to Roehampton modules&#8230;