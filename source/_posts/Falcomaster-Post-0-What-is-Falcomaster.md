---
title: 'Falcomaster Post #0: What is Falcomaster?'
date: 2017-08-09 16:12:51
tags:
---

Hi everyone! I'm Benji, a Norcal Jigglypuff player creating a program to play Super Smash Bros. Melee for the Nintendo GameCube. I started this development blog to keep everyone updated on my progress working on this project! :D

### What is Falcomaster

Falcomaster is going to be a supervised learning program that will mimic human
playstyles. It will watch a human play Melee, then it will learn to make choices
mimicking the human player.

Wait, what IS supervised learning? And how are we going to apply it to Falcomaster?

Supervised learning is a machine learning technique. Like many machine learning
techniques, it involves a program to be trained via training data. The training
data consists of an input and an expected output. In our case, the input would
be video frames/footage of gameplay, and the expected output would be the next
button press in the video.

The program would take in the video footage as part of training, and it will try
to "predict" the correct corresponding button to press. The correct buttons would be the buttons the human
player presses. Eventually, with enough
training data and time, the program will correctly predict the proper buttons
to press given any video frame, therefore copying a human's playstyle.

### Why Create Falcomaster

There is already work done in this space for Smash-related bots, in the form of
[SmashBot](https://github.com/altf4/SmashBot) by altf4 and
[Phillip](https://github.com/vladfi1/phillip) by vladfi1. Why start a whole new
project? Why not just add on to these wonderful existing projects?

There's a few reasons.

One, I really want to give it a try myself. I know I can just contribute to the
two existing projects as well, but I'd love to try my supervised learning approach,
which I don't think the other two projects use.

Two, my project works in a different niche than SmashBot and Phillip. SmashBot and Phillip are interested in creating the ultimate Melee AI, taking advantage of a computer's consistent ability to do superhuman input strings. Falcomaster, instead, just wants to copy a human.

Three, Falco is sick. Enough said.

I plan to look over the work done by altf4 and vladfi1. There are some traits that are shared in all our projects, such as imitating a GameCube controller's input.

### Who is Falcomaster

__

### More Questions?

I'm sure there are more questions that I didn't get to address in this article. Feel free to ask questions! I'll try to answer as many as I can :)
