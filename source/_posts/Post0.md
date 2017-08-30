---
title: 'Post #0: What is Falcomaster?'
date: 2017-08-12 16:12:51
tags:
---

Hi everyone! I'm Benji, a Norcal Jigglypuff player and UC Berkeley student creating a program to play Super Smash Bros. Melee for the Nintendo GameCube. I started this development blog to keep everyone updated on my progress working on this project! I'm not sure how often I will post (I don't want to commit to weekly posts if new developments don't happen weekly), but I will post as often as I can :D

My code will be up on GitHub as well, for those that want to follow. No code has been written yet, but the repositories will be found in the "About" section on this website! I'll also link the relevant GitHub repositories each time I post :)

### What is Falcomaster

Falcomaster is going to be a supervised learning program that will mimic human playstyles. It will watch a human play Melee, then it will learn to make choices mimicking the human player.

Wait, what IS supervised learning? And how does it apply to Falcomaster?
<!-- more -->
Supervised learning is a machine learning technique. It involves a program taking in training data (this is also known as "training a program"). The training data consists of an input and an expected output. Later, when it is presented with real data, the program can utilize its training to draw conclusions. If you want a more formal definition on supervised learning, Wikipedia has an article [here](https://en.wikipedia.org/wiki/Supervised_learning).

In our case, the input will be video frames/footage of gameplay, and the expected output will be the next button press in the video. The program will take in the video footage as part of training, and it will try to "predict" the correct corresponding button on a GameCube controller to press. The correct buttons will be the buttons the human player presses in the video. Eventually, with enough training data and time, the program will correctly predict the proper buttons to press in any gameplay situation, thus copying a human's playstyle.

For now, I'm planning to have Falcomaster run in computer environments alongside GameCube emulators, like Dolphin. But there is potential to port Falcomaster to run on a GameCube.

### Why Create Falcomaster

There is already work done in this space for Smash-related bots, in the form of [SmashBot](https://github.com/altf4/SmashBot) by altf4 and [Phillip](https://github.com/vladfi1/phillip) by vladfi1. Why start a whole new project? Why not just add on to these wonderful existing projects?

There's a few reasons.

One, I really want to give it a try myself. I know I can just contribute to the two existing projects as well, but I'd love to try my supervised learning approach, which I don't think the other two projects use.

Two, my project works in a different niche than the existing projects. SmashBot and Phillip are both interested in creating the ultimate Melee AI, taking advantage of a computer's consistent ability to do superhuman inputs. Falcomaster, instead, just wants to copy human behavior.

Three, Falco is sick. Enough said.

I plan to look over the work done by altf4 and vladfi1. There are some shared traits in all our projects, such as imitating GameCube controllers inputs. No need to start completely from scratch ;)

### Who is Falcomaster

There's a joke/urban legend/meme in the competitive Melee community about a player/entity named Falcomaster. It is said that no one knows who Falcomaster really is, but, once in a blue moon, Falcomaster will come to a tournament near you, destroy everyone, and leave without a trace.

I named this project after the urban legend Falcomaster...just because I thought it sounded cool :P

### More Questions?

I'm sure there are more questions that I didn't get to address in this article. Feel free to ask questions! I'll try to answer as many as I can :)
