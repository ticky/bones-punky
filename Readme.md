# Punky Pong

A restoration of Bones' Punky Pong flash game from 2009. Based on the archived version at <https://web.archive.org/web/20100113173616if_/http://www.fox.com/bones/features/game/>, which doesn't work.

As mentioned in _The Boney Island Whitefish in: Being Joel David Moore_, a Patreon bonus podcast for [Trashfuture](https://www.patreon.com/posts/boney-island-in-39157856) and [Boonta Vista](https://www.patreon.com/posts/boney-island-in-39156826) patrons.

I'm sad to say it's not very good; I wasted a lot of time on this. You'll need a browser with Flash enabled to run it. Those are becoming more and more rare!

<https://ticky.github.io/bones-punky/>

## How did you get it working?

Seeing that the Flash movie was attempting to fetch an `xml/config.xml` file unsuccessfully, I first attempted adding an XML file there, to no avail.

I then used the [FFDec / JPEXS Free Flash Decompiler](https://github.com/jindrapetrik/jpexs-decompiler) (pick a name!) to reverse-engineer what it was after.

Thankfully, the code used the standard [Flash XML API](https://help.adobe.com/en_US/FlashPlatform/reference/actionscript/3/XML.html) and it was pretty easy to find references to that in the decompiled code which showed that it needed an XML file with a root entity (of any name) which contained an `ads` entity with at least `url`, `showOnLoad` and `duration` properties, as well as a valid XML file at the supplied ads URL. I turned them off, which _isn't very preservationist of me_, but oh well.

Then, with it working, I set about archiving the surrounding web page, updating a bunch of URLs and pruning extraneous resources. This bit was probably more effort than I should've put in, but I wanted as much of the 2009 experience to be present. The original ads didn't get archived so I replaced them with something which seems period-appropriate.

And that's that!

## Copyright?

Not to be all "no copyright intended" or anything but this is for archival purposes only and I do not claim any ownership of any of the resources contained herein!
