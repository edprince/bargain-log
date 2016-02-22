---
layout: post
title:  "Inventory"
date:   2016-02-03 23:59:05
categories: jekyll update
---

I have just been working on implementing an inventory system for the game,
allowing the player to see which items they have, and how many of each. This
involves looping over the game items dictionary and displaying each in turn
followed by a variable (representing quantity), in the Pygame window.

{% highlight python %}
  placePosition = 10
  for i in game_items:
      DISPLAYSURF.blit(game_items[i], (placePosition, MAPHEIGHT * TILESIZE + 20))
      placePosition += 40
      textObj = INVFONT.render(str(inventory[i]), True, WHITE, BLACK)
      DISPLAYSURF.blit(textObj, (placePosition, MAPHEIGHT*TILESIZE + 20))
      placePosition += 60
{% endhighlight %}



[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
