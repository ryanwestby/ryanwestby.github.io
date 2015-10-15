---
layout: page
title:  "Djinn"
permalink: /projects/djinn.html
published: true
main_nav: false

project: true
project_description: "Space Invaders / Tetronimos Mashup written in Java using LWJGL"
project_image: "assets/images/djinn.png"
project_date: "Fall 2015"
---

__Project Date:__ {{ page.project_date }}

<small>__Technologies:__ Java, OpenGL, LWJGL, Slick2D</small>

For my first large project I recreated both Space Invaders and Tetronimos. The spin here is that both games are played at the same time. Tetronimos is played with the AWSD keys, while Space Invaders is played with the Arrow Keys and the Spacebar.

I had a lot of fun figuring out how to run Tetronimos properly and accurately. At initialization, an enum is created that holds every possible tetronimo and its rotations. While the game is running, a random tetronimo is produced and then controlled by the player and set such that complete lines are created. The game continually checks for collisions for blocks, walls, and enemy and player shots, and produces specific reactions to any instance of a collision. 

During play, each tetronimo fills into a HashMap where the keys are the y coordinate of the tetronimos and the HashMap's values are ArrayLists of the blocks at each y coordinate. Once the game has detected that the ArrayList of blocks at any y coordinate has reached a certain size, each block in that row is removed from the game and the rest of the block heights are shifted to fill in the empty space.

I'm looking forward to hosting the game online so that it can be playable on a web page. For now, you can see the code at my <a href="https://github.com/jryanwestby/Djinn">GitHub</a>.

<a href="{{ page.project_image | prepend: site.baseurl }}" data-lightbox="djinn" data-title="{{ page.project_description }}">
  <img src="{{ page.project_image | prepend: site.baseurl }}" title="{{ page.project_description }}">
</a>