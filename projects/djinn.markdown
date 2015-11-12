---
layout: page
title:  "Djinn"
permalink: /projects/djinn.html
published: true
main_nav: false

project: true
project_description: "Space Invaders / Tetronimos Mashup written in Java using LWJGL"
project_image: "assets/images/Djinn.gif"
project_date: "Fall 2015"
---

__Project Date:__ {{ page.project_date }}

<small>__Technologies:__ Java, OpenGL, LWJGL, Slick2D</small>

For my first large project I recreated both Space Invaders and Tetronimos. The spin here is that both games are played at the same time. Tetronimos is played with the AWSD keys, while Space Invaders is played with the Arrow Keys and the Spacebar.

I had a lot of fun figuring out how to run Tetronimos properly and accurately. At initialization, an enum is created that holds every possible tetronimo and its rotations. While the game is running, a random tetronimo is produced and then controlled by the player and set such that complete lines are created. The game continually checks for collisions for blocks, walls, and enemy and player shots, and produces specific reactions to any instance of a collision. The game runs until all invaders are removed, and ramps up difficulty as time progresses.

### Game Framework vs. Game Engine

In game dev, there is a distinction between engines and frameworks. An engine contains a comprehensive set of tools to help build a game from scratch. These might include a level editor, an asset manager, animation system, and a scripting language for the game’s logic. Code will need to be written for the engine, but the code here will be focused on game logic. Engines take care of the effort required at the system-level. Examples of game engines include Unreal Engine 4, Unity, and Construct 2.

A framework however will handle much less. They will typically take care of the OS-level window in which the game will run and provide a way to draw in that window (eg. OpenGL). A framework will also handle input devices and provide sound implementation. Beyond that, it’s up to the programmer. Examples of game frameworks include PyGame, Love, and LWJGL.

I chose to go with using a framework for Djinn because my focus was not to “make a game” but rather to use the programming of a game as a means to strengthen my skills. The framework allowed me to make my own decisions about the design and architecture of the game, without having this already laid out for me such as in the case of a game engine. I was also able to form a deeper understanding about the various moving parts of my game, without it being hidden under the hood of an engine.

### Program Details

During play, each tetronimo fills into a HashMap where the keys are the y coordinate of the tetronimos and the HashMap’s values are ArrayLists of the blocks at each y coordinate. Once the game has detected that the ArrayList of blocks at any y coordinate has reached the appropriate size, each block in that row is removed from the game. Code for the game can be seen at my <a href="https://github.com/jryanwestby/Djinn">GitHub</a>. Be sure to check out  EntityBlockHandler.java, where the logic for tetronimos is contained.

### Future of the Project

I'm looking forward to hosting the game online so that it can be playable on a web page. For now, here is a gif preview of the game:

<a href="{{ page.project_image | prepend: site.baseurl }}" data-lightbox="djinn" data-title="{{ page.project_description }}">
  <img src="{{ page.project_image | prepend: site.baseurl }}" title="{{ page.project_description }}">
</a>