---
id: 372
title: Open Source Presentation Tools
date: 2007-08-29T15:07:19+00:00
author: Miles Berry
layout: post
guid: http://milesberry.net/?p=372
permalink: /2007/08/open-source-presentation-tools/
categories:
  - Uncategorized
---
I&#8217;m struck by the extent to which PP has become synonymous with a computer based presentation these days, and have mixed feelings about its use in elementary or primary education. There&#8217;s no doubt that presenting to an audience of ones peers is a key skill these days, and I was hugely impressed by the research and polish that my 9-11 year olds put into their ESB presentations. The danger, of course, is that the software gets in the way of the research and analysis, and pupils become so excited about the possibilities which sound and vision open up that they concentrate on these rather than the content of their talk, and their interaction with their audience; something I know happened with my own classes in the past. It&#8217;s some indication of the extent to which primary aged pupils are already familiar with the bangs and whistles side of PP that even the <span style="text-decoration: line-through">DfES</span> DCSF see a need to begin senior school ICT with a [unit highlighting good and bad aspects of slide design](http://www.standards.dfes.gov.uk/secondary/keystage3/all/respub/ictsampley7), with the semi-ubiquitous example of [&#8220;Pat&#8217;s Poor Presentation&#8221;](http://www.google.co.uk/search?q=%22pat%27s+poor+presentation%22&ie=utf-8&oe=utf-8&aq=t&rls=org.mozilla:en-GB:official&client=firefox-a), and whilst attention is paid to the need for structure, particularly the use of PowerPoint&#8217;s (cited as an example) outliner, we do have one particular model of how to use slideware:

> an effective presentation is one in which the audience finds the information useful and interesting and where fonts, colours, images and sound are used in ways that catch their attention and help to get the information across.
> 
> <!--more-->

Which, I suspect, folks like [Edward Tufte](http://www.edwardtufte.com/tufte/powerpoint) and [Garr Reynolds](http://www.presentationzen.com/about.html) might take some issue with. So, in setting a presentation as an activity, what is important? There seem to be a number of bases to cover here:

  * **Research** &#8211; exploring the subject, discerning what matters and being selective, analyzing, making comparisons, telling stories, organizing things into a structure. And, of course, the content itself _does_ matter, and having 11 year olds spend the first six lessons of senior school ICT on producing a presentation to introduce themselves to their classmates seems a wasted opportunity, when so many aspects of other subject could be explored here.
  * **Use of the software** &#8211; there are skills to be learnt here, no matter how quickly learners pick up an interface: the example of PowerPoint&#8217;s outlining tool springs to mind, and yet, this is relatively low level stuff, we&#8217;re not, after all writing code here
  * **Design** &#8211; there&#8217;s a potential conflict here with the software skills, as it&#8217;s all too easy to focus on adding complexity and distractions when, I suspect, a really effective presentation, one that stands out from the crowd, has an elegant simplicity to its design. It&#8217;s possible that folk over in the art department might be better at teaching this than the ICT staff.
  * **The actual presenting bit** &#8211; again, something which ICT teachers _might_ not be the best folk to teach: I&#8217;m thinking cross-curricular projects with drama, English, history whatever, might have some real value here, and this is one aspect which the ESB presentation element has certainly helped my pupils towards.
  * **Reflection** &#8211; feedback from the audience, including the teacher(s), time to reflect on how the presentation went and what&#8217;s been learnt.

Of course, PowerPoint, when used well, isn&#8217;t going to stand in the way of achieving these objectives. That said, my ongoing exploration of ubuntu/edubuntu has provided some interesting insights into the world of presentation software that exists beyond PowerPoint.

The most obvious alternative is OpenOffice Impress, which is, I&#8217;d say, a pretty good substitute for PowerPoint. It&#8217;s a pretty good substitute for the MS product, without quite so many transition, animation and clipart effects, which given my views above, may be no bad thing. The outline tool is good, although it doesn&#8217;t have the interoperability with Writer that Word/PowerPoint have. One of the best things about Impress is its export capabilities, with native support for Flash and PDF.

Impress&#8217;s PDF export capabilities are particularly good when used alongside [KeyJNote](http://www.google.co.uk/url?sa=t&ct=res&cd=1&url=http%3A%2F%2Fkeyjnote.sourceforge.net%2F&ei=vmLVRpfiEZ6W0wSJ5uHRDA&usg=AFQjCNG54V2hEF662LwImSFDeoKlsKVd5w&sig2=jaZ1Zqw3j_w1lJ-wttVBeg) as a tool for viewing presentations. In the best traditions of Open Source, we have here a small program that does a single task very well, the task in this case being showing presentation slides &#8211; lots of command line or sidecar file based options, but in essence it provides eye-candy transitions, text and mouse highlighting, and a quick overview feature to use whilst running the presentation. Really nice software, which will work with directories of image files too. The Windows and Linux versions don&#8217;t even need installing (although the Linux one needs Python to work), making them ideal for storing on a USB stick alongside the presentation slides themselves.

The PDF export from Impress is also useful in conjunction with  [SuperShow](http://www.rastersoft.com/programas/supershow.html), which will combine the slides from the pdf with audio recorded  alongside and output a .swf file  of the whole presentation.

I have a lot of admiration for [LyX](http://www.lyx.org/)&#8216;s WYSIWYM approach to document creation, although I&#8217;ve not yet managed to give up the bad habits of messing with formats acquired through using Word. Using the [LaTeX Beamer](http://latex-beamer.sourceforge.net/) class, LyX is quite capable of producing some rather elegant presentation slides, which again feed beautifully into KeyJNote. I&#8217;m not convinced that this quite has the ease of use I&#8217;m looking for for primary work, but it does keep the focus very much on the content and the structure.

Elgg itself now has a presentation module, and whilst it&#8217;s not a bad way to share presentation content online, I can&#8217;t imagine many folk using it live with an audience: it&#8217;s probably best used as an e-portfolio tool, as [Helen Barrett](http://eduspaces.net/helenb/presentations/517) is. Something like [slideshare](http://www.slideshare.net/) or [GoogleApps&#8217;s long expected presentation tool](http://googleblog.blogspot.com/2007/04/were-expecting.html) is, I suspect, a more transparent way of publishing traditional slides. The social network dimension of these web-based applications has much going for it in terms of my reflection objective above: slideshare do seem to have got this right. Indeed, just as Flickr is a great resource for teaching photography, Slideshare would be a pretty good tool for teaching about presentation design. Alas, unlike gallery2 as an alternative to Flickr, I&#8217;m not aware of any open-source version which one could run inside a walled garden&#8230;

There are other interesting ways of using the web for presentations though. [Eric Meyer&#8217;s S5](http://meyerweb.com/eric/tools/s5/) is particularly impressive, although I&#8217;d be hesitant before going down the route of teaching the mark-up needed to primary children. S5 integration into Moodle and Elgg would be avenues worth exploring. Another cool idea is the [XUL based tool](http://www.bright-green.com/blog/2005_12_15/a_cute_mozilla_xul_app.html) that bright-green developed for [Takahashi style](http://presentationzen.blogs.com/presentationzen/2005/09/living_large_ta.html) minimalist presentations.

The research aspect that is a key part of presentation work in school as I see it is perhaps best achieved outside of the presentation software itself. Google notebook might be a starting point here, but of course, it&#8217;s not open source. For web-based research, del.icio.us has much to be said, and clever use of tagging would allow for some content organization on the fly, together with some interesting possibilities for collaborative research. There is a whole host of open source applications which replicate del.icou.us&#8217;s functionality, and in some cases API, such as scuttle. A wiki would also provide a way to collect source material together, and with a little organization, editing, and design work, could also be used for the presentation itself. An alternative approach, and one I&#8217;ve used successfully in the past, is to use mind mapping software such as freemind or semantik for this, and I think this provides a visual, accessible route in to the crucial sifting and organization dimension. There are interesting interoperabilities here: [semantik](http://freehackers.org/%7Etnagy/kdissert.html) (nee kdissert) is designed as an authoring / outlining tool, and will happily produce Beamer formatted LaTeX, [Freemind](http://freemind.sourceforge.net/wiki/index.php/Main_Page), on the other hand, has [mediawiki](http://www.wikimindmap.org/about.htm) and [del.icio.us](http://www.blainekendall.com/deliciousmind/) integration, both of which are very cool, although the wiki browser doesn&#8217;t appear to be GPLed :-(.

In fact, Freemind&#8217;s non-linear, strongly visual format would, if we weren&#8217;t so wedded to the linear format of the PowerPoint presentation, make it a very appealing tool for illustrating a presentation &#8211; certainly worth experimenting with, I think. Alternative approaches to presentations are undoubtedly of value. Much could be done using images alone, such as in iphoto or photostory: linux has [SlideshowCreator](http://slcreator.sourceforge.net/), but the interface is a bit OTT; there may be others out there! I have a vivid recollection of [Stephen Heppell](http://www.heppell.net/) presenting by just talking us through a number of pictures, documents, webpages etc that he&#8217;d gathered together in a folder on his PowerBook. There&#8217;s also something to be said for dispensing with the slideware entirely, and just talking to and interacting with the audience.