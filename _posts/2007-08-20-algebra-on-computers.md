---
id: 374
title: Algebra on Computers
date: 2007-08-20T16:06:07+00:00
author: Miles Berry
layout: post 
comments: true
guid: http://milesberry.net/?p=374
permalink: /2007/08/algebra-on-computers/
categories:
  - Uncategorized
---
A couple of interesting updates today from [Chris Sangwin](http://web.mat.bham.ac.uk/C.J.Sangwin/) at Birmingham University.

<!--more-->

Anyone who&#8217;s ever done any maths on a computer involving concepts as advanced as fractions will be familiar with the difficulty in inputting or outputting mathematical expressions, hence such notions as Donald Knuth&#8217;s [T<sub>E</sub>X](http://en.wikipedia.org/wiki/TeX) and MathML. Although maths should lend itself to computer based assessment ([Gödel&#8217;s incompleteness theorem](http://en.wikipedia.org/wiki/G%C3%B6del%27s%20incompleteness%20theorems) notwithstanding, things are generally right or wrong), these input/output issues soon get in the way. Moodle&#8217;s splendid T<sub>E</sub>X filter does much to help with the output side of things, although even this doesn&#8217;t have the same WYSIWYG functionality teachers or students today perhaps expect. Chris has co-authored [a paper](http://web.mat.bham.ac.uk/C.J.Sangwin/Publications/2007-Sangwin_Ramsden_Syntax.pdf) which explores some of the input issues in more detail.

To help with this, Chris and Alex Billingsley have produced [DragMath](http://web.mat.bham.ac.uk/C.J.Sangwin/dragmath/), a rather nice little Java applet which lets you drag and drop a whole host of mathematical symbols around, and then produces code in a format which computer algebra systems like Maxima and Maple, or L<sup>A</sup>T<sub>E</sub>X or MathML can interpret correctly. Very nice work, and better still, Open Source, with the project over on [Sourceforge](http://sourceforge.net/projects/dragmath).

Chris&#8217;s [STACK](http://stack.bham.ac.uk/stack/) project also continues development. STACK is an online assessment tool for mathematics, with a computer algebra system, in this case the open source, and very splendid, [Maxima](http://maxima.sourceforge.net/), running in the background. Thus, Chris has an assessment system which understands matematics, and so questions like &#8220;Give a fraction equivalent to 1/4&#8221;, and &#8220;Factorise x<sup>2</sup>+5x+6&#8243; become things which can be marked automatically without having to type in semi-infinite lists of alternative expressions.

There&#8217;s been attempts at getting Moodle and Stack to talk since, I think, Moodle 1.5 in Spring 2005, but whilst I played with this I never managed to get it working. The [future of STACK](http://mantis.york.ac.uk/moodle/mod/forum/discuss.php?d=953) looks like being as a fully integrated Moodle module, together with some support for more intuitive, interactive interfaces such as DragMath above, and the java based open-source interactive geometry tool [GeoGebra](http://www.geogebra.org/cms/).

_<http://eduspaces.net/mberry/weblog/190539.html>_