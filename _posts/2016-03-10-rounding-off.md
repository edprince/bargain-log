---
layout: post
title:  "Rounding off"
date:   2016-03-10 23:13:05
categories: jekyll update
---

Coming to the end of the project, we have done our presentation, received
feedback on usability and touched up. We have improved a few things, including
the bug that was stopping the items from displaying in the inventory correctly.

#Individual Feature#

I have added an extra feature that tracks all the robots movements, displays on
the map where it has been, and calculates what percentage of the map has been
covered.

![Traced-map](http://i.imgur.com/cxH6P2q.png)

In order to calculate the percentage of the map covered, I wrote the following
function:

{% highlight python %}
def calculate_percentage(covered, totalW, totalH):
    '''Function calculate how much of map is visited
    Takes 2 lists and compares to see how much of the ground has been visited'''
    uniqueTiles = 0
    for i in range(totalW):
        for j in range(totalH):
            if ([i, j] in covered):
                uniqueTiles += 1
    return (uniqueTiles / (totalW * totalH)) * 100
{% endhighlight %}

###Evaluation of the project###

Overall I think the project has been mixed with regards to it's success, there
are some things I feel have worked very well, and other aspects that can without
doubt be chalked down to experience. 

The first successful area of this project has been its management, and use of
software to keep everybody up to date with progress.

![Github octocat](http://quickfixes.github.io/just-gittin-started/img/octocat.png)

The place to begin is with the most important management tool of the lot - GitHub.
It has been vital for the progress and success of this project, that we successfully 
used a version control system. GitHub has been magnificent, and although confusing for
some members of the team who had never used it before, proved invaluable right the way
to the end. We were able to commit code, revert to earlier builds, use branches for individual
features, raise issues, assign tasks, view each others work, and integrate other software.

Other such software included Travis CI.

![Travis CI logo](https://workablehr.s3.amazonaws.com/uploads/account/logo/11901/large_Mascot-fullcolor-png.png)

Although for this project, it was largely irrelevant, Travis was a really cool
service to successfully employ, more as an investment for future projects. With
Travis CI, I was able to write unit tests that could test functions, and every
time any code was commited, it would run the tests to make sure the functions
were still being run correctly, if not, it would fail the build, alert me via
email, and change the badge on the repository readme to 'build: failing'.

Lastly, I feel the presentation was done well, and possibly the first time the
group really pulled together a bit more. I think future projects will require
far more communication, better delegation of work to individuals, and a more in
depth analysis at the start, with a stronger focus on design. As a process, it
has been fantastic, and very, very rewarding, seeing a project come from pen and
paper, to a real product. And that's it from me for this project.

Follow me on Twitter and GitHub to keep up to date with my work, and to see more
blogs on future projects.



[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
