---
layout: post
title:  "Creating a prototype for the game"
date:   2016-02-09 09:08:05
categories: jekyll update
---
This week I have started work on a prototype version of the game. This is
involving a very simple, abstracted version of our final game. The prototype
generates 5 instances of different item objects, and displays them on the screen
at wherever their coordinate attributes state they should be. Currently each
item is only being represented by a blue circle. Then a player is generated, and
placed in the centre of the map. I then need to work on the automatic movement
algorithm that will allow the sprite to move efficiently from item to item.

##The Algorithm##
The first idea I've had for the algorithm is a very simple concept. Essentially
the idea is to calculate the distance between the player and the item it is
searching for, and make a random movement (left, right, up, down). Then
calculate the distance once more and see if the sprite is moving in the correct
direction. 

{% highlight python %}
def calculate_distance(x1, y1, x2, y2):
  #Getting the absolute height and width values
  width = math.sqrt((x2 - x1)**2)
  height = math.sqrt((y2 - y1)**2)
  return math.sqrt(width**2 + height**2)
{% endhighlight %}

On a map with no obstacles, this would work, but our map will contain
tiles through which the sprites cannot pass through. This means more complex
algorithms will be needed in order to efficiently move the automatic sprite
around the screen.



[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
