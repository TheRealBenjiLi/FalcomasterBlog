---
title: "Post #2: Heat Waves and Future Challenges"
tags:
---
Over the last two weeks, the Bay Area where I live was hit with a massive heat wave. Unfortunately, the Bay Area is not used to high temperatures, so there are no air conditioners where I live. Around the same time, I got a cold. So instead of working on the Falcomaster project, I spent time getting myself back onto my feet and catching up on all the schoolwork I neglected as I was sick >.<

This means I don't have any real progress to report. Instead, I'll use this post to discuss other things about this project :)
<!-- more -->

### A Powerful Machine
My laptop is not ideal to run Dolphin, the GameCube emulator. By the time I finish the code for Falcomaster (or at least, the majority of it), I'll need a powerful-enough machine that could play Melee (without input lag!) and record the game footage, to be used as training data for Falcomaster.

I found a suitable candidate in the computer science building. One of the on-campus clubs, the Computer Science Undergraduate Association, has a plethora of powerful desktop computers in their office, available to all its members. These machine will likely be the ones I use to record game footage.

However, training data needs an input and an expected output. In our case, for each frame of video footage, there must be some "correct" answer, answering the question "What is the next button pressed by the Falco player?". Only with both of these can I construct a proper training dataset.

So what exactly is the issue? Well, the Memory Watcher feature I was planning to use to record button inputs is (from what I can tell) a Linux-only feature. The CSUA machines are all using the Windows operating system by default. Because of this, there's a possibility that whatever I create on my laptop won't work when I want to record training data in the CSUA office! D:

While I have no immediate fix to this, this will be an interesting challenge in the future, assuming Memory Watcher only works in Linux systems.

### Scalability
Let's continue discussing the Memory Watcher from earlier :D

The Memory Watcher is a feature built into the Dolphin emulator that allows users to read memory addresses used by the game. This is useful when debugging games or trying to understand how the game operates at a low level. I found in my last post that Melee keeps track of the controller state in the game's memory, so I'm using the Memory Watcher to read the controller state, giving me insight on what buttons are pressed.

However, committing to using the Memory Watcher creates a future obstacle. Falcomaster's potential, in theory, is not limited to Melee. The ability to copy a player's habits in a video game through supervised learning is universal to all GameCube games. Theoretically, the technology for Falcomaster could be applied to any game, but if I choose to use Memory Watcher as the method to read GameCube controller inputs, Falcomaster's application will likely be limited to just Super Smash Bros. Melee D:

The reason why I say this is because there's no guarantee all GameCube games store the controller state in memory, and even if they do, there's no guarantee they all store it in the same memory addresses.

While this is an issue, it's not a major one yet. After all, my current intention with this project is for its application in Melee. But if I ever choose to use Falcomaster on other games, the Memory Watcher approach will come back to haunt me.

### Last Thoughts
In closing, I got sick, and didn't make any progress. I explore design challenges that may arise in the future instead of discussing the progress I didn't make :P

I plan to show some more results in my next post. Stay tuned, everyone! <3
