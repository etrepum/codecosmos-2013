% Teaching with CodeCosmos
% Bob Ippolito
% RuPy 2013<br/>Budapest, Hungary

# How did I get here?

- Using computers since before I could read
- Professionally since 1997
- Founded a company and had a successful exit
- Ended up with a normal job by accident
- Wasn't passionate about it

# {#z160}

<img src="img/z160.jpg" class="landscape" alt="Zenith Z-160"/>

# {#kq1}

<img src="img/Kings_Quest_Tandy.png" class="landscape"
  alt="Kings Quest I"/>

# Finding a mission

- Wanted to do some social good
- Why not education?
- I know how to teach myself programming
- Can I teach others?

# {#ewd}

<h2>It does not suffice to hone your own intellect (that will join you in your grave), you must teach others how to hone theirs.</h2>
&ndash; E.W. Dijkstra (<a href="https://twitter.com/DijkstraQuotes/status/357546511841763329">@DijkstraQuotes</a>)

# {#eg7-badge}

<img src="img/61523_10151575635106253_749096641_n.jpg"
class="portrait" alt="EG7 badge"/>

# EG7

- Attended a wonderful conference with great people
- Met COO of The College Initiative

# {#jpl}

<img src="img/jpl.jpg" class="landscape" alt="Curiosity at JPL" />

# The College Initiative

- Non-profit assistance for High School students
- Summer program to help prepare for college
- Why not open their minds to programming?

# {#i-have-no-idea}

<img src="img/i-have-no-idea.jpg" class="landscape" alt="I have no idea what I'm doing"/>

# Can I use a service?

* Khan Academy had no teaching tool
* Codeacademy had technical issues
* Could I make it work?

# {#nope}

<img src="img/unplugged-internet.jpg" class="landscape" alt="Unplugged internet"/>

# Planning to build

* I need it to work without internet
* I want it to also work online
* I don't want to install anything
* Can depend on Chrome

# Language

* JavaScript is the only viable in-browser language
* Can't do better given only a few weeks

# Canvas

* Strings aren't interesting to today's students
* Khan Academy uses Processing.js
* I knew others who have taught with Processing
* Couldn't find a similar library that did a better job

# Editing

* I looked at Ace because Khan Academy uses it
* CodeMirror also had a lot of street cred (WebKit inspector)
* I found CodeMirror's examples to be easier to understand
* CodeMirror works great

# {#editing-in-action}

<img src="img/codecosmos-tree.png" class="landscape" alt="CodeCosmos editor"/>

# Linting

* JavaScript syntax is hard, so linting is essential
* JSHint worked particularly well
* CodeMirror ships with an example
* I moved it to a Web Worker for performance reasons

# JavaScript :( {#javascript}

* JavaScript sandboxing isn't a thing
* Web Workers can't talk to a canvas
* iframes don't execute concurrently
* How can I cheat?

# Cheating

* Increment a counter for function calls and loop iterations
* If the counter gets too big, abort!

# Rewriting JavaScript

* Parse with Esprima
* Transform with Estraverse (insert cheats)
* Write back out with Escodegen
* Eval directly, not in a Web Worker

# {#sandboxing-in-action}

<img src="img/codecosmos-sandbox.png" class="landscape" alt="CodeCosmos sandbox"/>

# {#wtf-before}

<div class="bigger">
```javascript
var wtf = function (a, b, arr) {
  arr.forEach(wtf);
};
wtf(null, null, [1]);
```
</div>

# {#wtf-after}

<div class="bigger">
```javascript
'use strict';
var __f = __catchErrors(
  function __userCode$1() {
    var wtf = __catchErrors(
      function wtf$1(a, b, arr) {
        if (++__ctr >= __maxctr) {
          __cont = false;
          throw new Error('…');
        }
        arr.forEach(wtf);
      });
      wtf(null, null, [1]);
  });
__f();
```
</div>

# Web App

* AngularJS
* Font.js
* jQuery
* JSZipTools
* Underscore

# Persistence

* PouchDB
* CouchDB
* follow, request, node-static

# {#persistence-in-action}

<img src="img/codecosmos-persistence.png" class="landscape" alt="CodeCosmos persistence"/>

# Build tools

* Grunt
* Bower

# CSS and Fonts

* Pure CSS
* <span class="font-awesome icon-thumbs-up"></span> Font Awesome <span class="font-awesome icon-heart"></span>
* <span class="kontrapunkt">Kontrapunkt Bold</span>
* <span class="source-code-pro">Source Code Pro</span>
* <span class="ubuntu-regular">Ubuntu Regular</span>

# {#twitter-login}

<img src="img/twitter-login.jpg" class="landscape" alt="Twitter Login"/>

# {#codecosmos-login}

<img src="img/codecosmos-login.jpg" class="landscape" alt="CodeCosmos login"/>

# Hosting v0

* My laptop

# Hosting v1

* GitHub pages
* Iris Couch
* Nodejitsu

# Hosting v2

<img src="img/rackspace-logo.svg" alt="Rackspace Logo"/>

* CouchDB + custom module
* No more node.js

# {#courier-index}

<img src="img/946585_272865049520270_623477349_n.jpg"
    class="portrait"
    alt="The Courier-Index front-page featuring Jamie and me"/>

# Lee County Senior High

* No cell coverage
* No internet connectivity
* Wasn't quite prepared
* But I had local copies of what I needed

# {#me-circa-1992}

<video src="img/me.mp4" poster="img/vid-me-1992.jpg" controls class="landscape"></video>

# {#monday-challenge-line}

<img src="img/challenge-monday-line.png"
    class="landscape"
    alt="Lines &amp; coordinates"/>

# {#alchemy-memphis}

<img src="img/alchemy-drinks.jpg"
    class="portrait"
    alt="Dinner &amp; drinks at Alchemy in Memphis"/>

# {#tuesday-help-student}

<img src="img/585_271796256293816_431985305_n.jpg"
    class="portrait"
    alt="Helping a student sort out a syntax error in her code" />

# {#olympic-rings}

<img src="img/Olympic_Rings.svg"
    class="landscape"
    alt="Olympic Rings"/>

# {#ashlee-rgb}

<img src="img/941238_272092032930905_2019553029_n.jpg"
    class="portrait"
    alt="Ashlee discovering how to make yellow from RGB components during the Olympic Rings challenge"/>

# {#jim-neelys}

<img src="img/1069390_10151721359976253_1227452275_n.jpg"
    class="landscape"
    alt="Jim Neely's Interstate BBQ in Memphis" />

# {#wednesday-don-knuth}

<video src="img/The Electronic Coach - YouTube [360p].mp4"
    poster="img/vid-don-knuth.jpg" controls class="landscape"></video>

# {#brasha-rings}

<img src="img/21399_272093619597413_58531329_n.jpg"
    class="portrait"
    alt="Brasha is stoked that she got the colors and pattern right for the Olympic rings" />

# {#ground-zero}

<img src="img/21385_4993070635857_656989762_n.jpg"
    class="portrait"
    alt="TCI staff night out at Ground Zero!">

# {#thurs-day-in-the-life}

<video src="img/A_Day_in_the_Life_-_Computer_Programmer.mp4"
    poster="img/vid-computer-programmer.jpg"
    controls class="landscape"></video>

# {#grl-shirt}

<img src="img/941227_272586392881469_1113510962_n.jpg"
    class="portrait"
    alt="Note the Graffiti Research Lab t-shirt :)"/>

# {#jordan-3d-triangle}

<img src="img/578361_272578132882295_17954676_n.jpg"
     class="portrait"
     alt="Jordan managed to make his Sierpinski triangle look like it's 3D"/>

# {#fractals}

<img src="img/970404_272577056215736_462365543_n.jpg"
     class="portrait"
     alt="Fractals in the classroom"/>

# {#fat-babys-catfish}

<img src="img/969738_10151725200766253_130031342_n-square.jpg"
     class="portrait"
     alt="Catfish lover parking only - all others will be pan-fried (at Fat Baby's Catfish House in Cleveland)"/>

# {#friday-books}

<img src="img/993051_10151719747726253_1827182736_n.jpg"
     class="portrait"
     alt="The Nature of Code (and other programming books)"/>

# {#students-and-staff}

<img src="img/1005752_272928776180564_364959941_n.jpg"
     class="portrait"
     alt="TCI students and staff after our last day of coding class"/>

# {#thank-you-card}

<img src="img/969338_10151726640286253_1988588723_n.jpg"
     class="portrait"
     alt="Fantastic thank you card from the students"/>

# {#rooftop-bar}

<img src="img/1001874_10151726866646253_1491639192_n.jpg"
     class="landscape"
     alt="Madison Hotel's rooftop bar in Memphis at sunset"/>

# {#gus-fried-chicken}

<img src="img/1005284_10151728747961253_1719802718_n.jpg"
     class="landscape"
     alt="Gus's Fried Chicken in Memphis"/>

# What's next?

* [exercism.io](http://exercism.io)
* More volunteering
* Keep looking for inspiration
* Any ideas? Would love to hear them

# Thanks!

+-------------+----------------------------------------------+
| **Slides**  | <http://bob.ippoli.to/codecosmos-2013/>      |
+-------------+----------------------------------------------+
| **Source**  | [github.com/etrepum/codecosmos-2013]         |
+-------------+----------------------------------------------+
| **Email**   | bob@redivi.com                               |
+-------------+----------------------------------------------+
| **Twitter** | @etrepum                                     |
+-------------+----------------------------------------------+

[github.com/etrepum/codecosmos-2013]: https://github.com/etrepum/codecosmos-2013


