---
title: 'Post #1: Controller Inputs and Memory Watcher Discoveries'
date: 2017-08-29 20:24:20
tags:
---


For Falcomaster, the first goal is to find out how to record GameCube controller inputs. This is vital for our training data. As mentioned in [Post #0](http://www.falcomaster.tech/2017/08/12/Post0/), the training data for our program needs an input (video game footage) and an expected output (button presses). We need to record controller inputs alongside video footage in order to deliver proper training data.

After many days of researching how to do this (I kept hitting brick walls, only to realize there were other easier solutions to try), I found something promising.
<!-- more -->

### Finding Memory Addresses

I found a [merged pull request](https://github.com/dolphin-emu/dolphin/pull/3403) made by spxtr on the Dolphin repository about a feature called Memory Watcher. Using the Memory Watcher gives you data about specific memory addresses used by the game.

Maybe I could find what memory addresses are used by Super Smash Bros. Melee to keep track of the controller state. I opened up Dolphin's debug mode (I didn't know Dolphin had a debug mode before this. Wow!) and started searching for memory addresses related with the controller. If I moved the analog stick, which memory addresses changed? How about if I pushed the A button?

I did this for about ten minutes before I stopped myself. The Melee community is full of people that pour their heart and soul into the game and dissect it for data. For example, the famous Smash player [Mew2King](https://www.ssbwiki.com/Smasher:Mew2King) once wrote [this](https://smashboards.com/threads/ssbm-statistics-list.30064/), which is still used today to understand Melee's inner workings. If there are people like Mew2King in the Smash community, surely there is someone that has already spent the time to scavenge through Melee's memory addresses and deduce what they do, right?

Sure enough, it's been done years ago, and is proudly displayed [here](https://docs.google.com/spreadsheets/d/1JX2w-r2fuvWuNgGb6D3Cs4wHQKLFegZe2jhbBuIhCG8/edit#gid=12). Good thing I didn't spend too much time looking for memory address data in debug mode myself :D

### Reading Memory Addresses

Now that I knew what memory addresses to look for, I just need to activate the Memory Watcher and focus on those addresses! Except...how do I do that? It's not exactly a checkbox that you tick in the Dolphin options. I spend a few days looking through the pull request instructions, only to be more and more confused. It no doubt works; people have done it before in many other projects. But my long search trying to understand how to use it led to very little results.

With enough searching, I may have stumbled on an answer. The creator of the Memory Watcher add-on, [spxtr](https://github.com/spxtr), also created code to write a Melee bot called [p3](https://github.com/spxtr/p3). p3 includes a Python implementation of using the Memory Watcher. Sweet! :3

That wraps up all my progress so far. I learned about the Memory Watcher feature and which memory addresses to look at (hopefully). The next step is to dive into spxtr's p3 program. I plan to investigate his Python implementation of using Memory Watcher, and modify it. Instead of using Memory Watcher for a bot, I will use it just to record inputs.
