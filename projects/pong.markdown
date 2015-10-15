---
layout: page
title:  "pong"
permalink: /projects/pong.html
published: true
main_nav: false

small_project: true
project_description: "Pong clone written in Python and Pygame using OOP"
project_image: "assets/images/pong.png"
project_date: "Spring 2015"
---

__Project Date:__ {{ page.project_date }}

<small>__Technologies:__ Python, pygame</small>

<a href="{{ page.project_image | prepend: site.baseurl }}" data-lightbox="djinn" data-title="{{ page.project_description }}">
  <img src="{{ page.project_image | prepend: site.baseurl }}" title="{{ page.project_description }}">
</a>

I used my first project as an introduction to Python programming and game concepts such as movement, control, collision detection, scoring, and artificial intelligence. I also took the opportunity to practice Object-Oriented Programming for my program design. Take a look at the code on my <a href="https://github.com/jryanwestby/pong">GitHub</a>.