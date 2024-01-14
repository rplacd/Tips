
<img width="43" alt="Screenshot 2024-01-13 at 7 26 30 PM" src="https://github.com/rplacd/Tips/assets/147152/2d039133-3abb-4fb6-b7e3-26a0b6daff0a">

About *Tips*
============

<img width="334" alt="Screenshot 2024-01-13 at 7 23 56 PM" src="https://github.com/rplacd/Tips/assets/147152/7023e6c5-fedc-4c0e-8adc-cb15495579a4">

Built to learn the basics of Pascal and classic Macintosh development, *Tips* is a toy that displays tips. Drag it to your Startup Items folder if you want tips every startup, like Windows 95 did. It is compatible with all classic Systems/Mac OS versions from 6.0.5 onwards.

*Tips* was written in THINK Pascal 4.0 (Symantec), after initial prototyping with AppMaker 1.5.4 (Bowers Development Corp), provides a lot of the boilerplate. It was developed in the emulation environment Infinite Macintosh (Mihai Parparita), and with the help of THINK Reference (Symantec).

*Public domain, questionable polish, etc.*

*Known bugs and infelicities.*
  
- On Macintoshes (a) running Systems less than 7, and (b) with a 512 x 342 display (e.g. compact Macs), the title text "Welcome to System 6" cuts the 6 short.
– Since we use the Gestalt Manager to obtain the System version, compatibility is limited to System 6.0.5 onwards. Despite being a very simple application.
- Closing the app on 68000-based Macs takes a long time. I'm not sure why. Perhaps it's AppMaker's boilerplate.

Contents
--------
This repository contains

- A Stuffit file with the built application.
- A '.dsk' disk image with the application source, and all of its dependencies: THINK Pascal and AppMaker's libraries. Use this to develop.
- *Partial* source in plaintext for your online viewing pleasure -- that is, leaving out THINK Pascal and AppMaker source code, resource forks, etc.

Setting up development
----------------------
Mount the disk image in System 6.0.5 onwards. The THINK Pascal project is at the path Tips ƒ:Tips.π. With luck, because THINK Pascal is distributed with the development disk, you should be able to double-clock Tips.π to get started.

Adding your own tips
--------------------
The current set of tips exists in two places:

- hardcoded, in *TipsResources.p*;
- and the working copies of all of the tips exists in the 'tips' resources of the app.

The cleanest way to add new tips is to edit, in *TipsResources.p*:

- *NumTips*, the constant;
- *DoReinitializeTips*, the procedure, which clears out all of the working 'tips' resources with the tips hardocded into this function.

Then recompile the application, run it, and click the menu item Files > Reinitialize Tips and Quit.
