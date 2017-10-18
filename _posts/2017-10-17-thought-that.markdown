---
title: "Thought That"
layout: post
date: 2017-10-17 18:10
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: "React.js, Node.js, Express, PostgreSQL project to display currently trending topics and Reddit users' thoughts."
category: project
author: johndoe
externalLink: false
---

Link: [http://www.thoughtth.at/](http://www.thoughtth.at/)

This is a list of games that are most commonly mentioned in Reddit's
[Weekly /r/Games Discussion - What have you been playing, and what do you think of it?](https://www.reddit.com/r/Games/search?q=author%3AGamingBot+OR+author%3AAutoModerator+AND+playing&restrict_sr=on&sort=new&t=all)
threads.

Each game's page displays the comments that have mentioned the game's title. For games that have lasted for more than
two weeks, a chart of mentions over time will be displayed.

A worker is setup to check for new game releases, Reddit threads, and replies.

## Technologies

* React
* Node
* Express
* PostgreSQL
* Sequelize
* Bootstrap
