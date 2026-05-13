DripBot
============

Makes dripstat fun again.  Plays the game at <https://dropstatgame.solant.me/> optimally and automatically.

*DripBot is an autoclicker as well!*  Dripbot defaults to not clicking, and when it does click uses an algorith to attempt to appear human.  Although the algorithm is pretty good, *USE AT YOUR OWN RISK.*
The pops from clicking and global dripping are on by default, and can be toggled with `$dripBot.setShowPops(bool);`, where `bool` is a boolean value (true/false).  Defaults to false.

Usage
-----
Use a bookmark to easily start DripBot.  Create a new bookmark with `javascript:(function(){$.getScript('https://redmanmale.com/DripBot/dripBot.js');}());` as the *url*.  Then just head over to [dripstat](https://dropstatgame.solant.me), and once the page loads click your bookmark.

*or*

After loading dripstat, paste the following into your browser's console and press Enter: `$.getScript('https://redmanmale.com/DripBot/dripBot.js');`

For more information on browser consoles, see <http://webmasters.stackexchange.com/questions/8525/how-to-open-the-javascript-console-in-different-browsers> (YMMV).


Stages
------

1. *Story:* Traverses the story, starting the game from any point.
2. *Purchase:* Builds B/s as fast as possible, optimizing powerup and upgrade purchases with minimal dripping (dripping is waste).  Runs untill a B/s threshold is reached.  The threshold can be changed with `$dripBot.setBPSThreshold(float);`, where `float` is the desired threshold in MB/s.  Defaults to 7.
3. *Win:* Attempts to climb to first place by dripping constantly, and optionally stops when achieved.  Whether to drip when in first place or not can be toggled with `$dripBot.setBenevolentLeader(bool);`, where `bool` is a boolean value (true/false).  Defaults to false.


Diff from original
---

* fixed for new DripStat version
* restored missing assets
* disabled autoclicker pause
* show real bps value
