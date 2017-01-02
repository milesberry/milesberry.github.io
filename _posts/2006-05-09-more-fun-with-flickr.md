---
id: 292
title: More fun with Flickr
date: 2006-05-09T13:30:19+00:00
author: Miles Berry
layout: post
guid: http://milesberry.net/?p=292
permalink: /2006/05/more-fun-with-flickr/
categories:
  - Uncategorized
---
Thinking more about ways of using Flickr in the classroom, I&#8217;ve discovered the wonderful world of [geotagging](http://en.wikipedia.org/wiki/Geotagging). Essentially, all this involves is attaching geographical metadata to content, in this case Flickr photos. This then makes it possible to integrate the photos into maps, such as Google Maps or Google Earth.

<!--more-->

Considering the simplicity of the idea, the potential here is tremendous: in the classroom for example, not only can young geographers locate places on their Goolge Earth/Maps, but they can then find out a whole lot more about what the places are actually like on the ground, and perhaps something more about the people who live, work or visit there via Flickr profiles and streams. Clare and I were were really impressed by [eye2eye&#8217;](http://www.eye2eyesoft.co.uk/)s collection of UK photos at BETT, but here&#8217;s a way of doing the same sort of thing worldwide, for free, with Flickr as the image store, and  Google&#8217;s gorgeous, clickable, draggable satelite imaging.

More importantly, the cool thing about Web 2.0 is that schools, teachers and pupils can contribute their own photos and other content into the system. This is, of course, not too far removed from the wholly laudable (and open source) [Geograph](http://www.geograph.org.uk/), but the notion of using a Google Maps [mashup](http://en.wikipedia.org/wiki/Mashup_%28web_application_hybrid%29) (or a Google Earth layer) to pull together the sort of situated information provided through the [20 year old Domesday Project](http://www.atsf.co.uk/dottext/domesday.html) or [Wikiville](http://www.wikiville.org.uk/index.php/Main_Page), is a very appealing one. I can see this having huge possibilities for schools, and love the idea of pupils contributing pictures and desciptions of their own localities and field trips.

Now for the techie bit. Taking the pictures and uploading into Flickr&#8217;s the easy bit. There are a number of ways of adding in the essential geographical information (which has to be in latitude and longitude &#8211; another teaching opportunity):

  * You could do it by hand, if you can work out the latidude and longitude of the photo&#8217;s location &#8211; not easy, even with an OS grid map, as the conversion from OS grid reference to latitude and longitude is non-trivial, although StreetMap&#8217;s [converter](http://streetmap.co.uk/streetmap.dll?GridConvert?name=gu27%202es&type=PostCode) might be useful.
  * [Flickrmap](http://www.flickrmap.com/) have a [plugin](http://flickrmap.com/geotag/googleearth.php) for Google Earth &#8211; find the place in Google Earth and then click the pop up to tag one or more photos.
  * If you use Firefox and [Greasemonkey](http://greasemonkey.mozdev.org/), you can run the [GMiF](http://webdev.yuan.cc/gmif/) (Google Maps in Flickr) script , that lets you specify location picture by picture.
  * [maps.yuan.cc](http://maps.yuan.cc/) is a brilliant AJAX googlemaps mashup that allows you to browse flickr photos alongside a worldmap &#8211; if you give it read/write permission to your flickr stream, you can use it to browse through your photos, then zoom in to the place they were taken on the map and add all the tags directly &#8211; this is definitely the easiest of these three.
  * If you&#8217;ve got a GPS locator that can log way points, then it&#8217;s possible to attach that data directly to the photos themselves alongside the exif data, but this looks a bit complicated and I don&#8217;t have GPS so haven&#8217;t properly investigated &#8211; there&#8217;s a good introduction [here](http://www.macdevcenter.com/pub/a/mac/2004/06/15/gps_photo.html).
  * Rumour has it that built in GPS will be the next big thing in digital photography, so all the tagging will happen automatically in the camera. We shall see.

The other side of the process is being able to browse the pictures from a map, rather than simply see where each was taken. Again, there a number of possibilities, but at present they all suffer becuase they work with extracts of the Flickr database, rather than all <span class="DateTime">183,861 </span> <span class="DateTime">geotagged photos that Flickr knows about at the moment.<br /> </span>

  * [Flickrmap](http://www.flickrmap.com/) will provide a flash map of your own photos for $5 pa, which you can embed in a webpage.
  * They also make available [a layer](http://www.flickrmap.com/geotag/flickr_photos.kmz) for Google Earth, and there&#8217;s [a similar layer](http://maps.yuan.cc/api.php?method=flickr.search&mode=kml&flickr_id=) from Yuan.cc maps, which plot photo locations and then opens up a little pop-up with the photo.
  * Personally, I like the [maps.yuan.cc](http://maps.yuan.cc/) interface for browsing as well as tagging, here&#8217;s the [assembled collection for central Florence](http://maps.yuan.cc/?lat=43.7715896488274&lon=11.250085830688477&zoom=16&service=flickr).
  * Again, there&#8217;s a rumour that Flickr will do all this themselves soon, so this side of things will suddenly become a whole lot easier.

Finally, and more personally, here are [the photos](http://www.flickr.com/photos/mberry/tags/geotagged/) from my Flickr set that I&#8217;ve geotagged so far.

_<http://eduspaces.net/mberry/weblog/14188.html>_