---
layout: post
title:  "Framerate issues and timer"
date:   2016-02-22 12:21:05
categories: jekyll update
---
Today I have been working on fixing the incredibly slow framerate. After some
research, we discovered that using DOUBLEBUF as a flag for the
`display.set_mode()` improves this slightly, but still nowhere near the level we
wanted/needed. After some testing, and narrowing down, I found that it was the
`.fill()` method being used that slowed the game down enormously. So I removed
this and used the `.blit()` method, filling the screen with a tile instead. This
dramatically improved our frame rate to a level we were happy with.

I was also working today on the timer for the project. The specifications state
that the user should be able to enter a time that counts down, meaning the robot
only has a set amount of time to collect items. This can be done very easily
with pygame, using it's built-in `pygame.time.set_timer()` method, allowing a
number of milliseconds to be specified before fulfilling a condition. From there
a function can be called to bring up the scoreboard.



[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
