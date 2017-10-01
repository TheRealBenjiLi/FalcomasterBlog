---
title: "Post #3: IT SPEAKS!"
tags:
---
As you can probably tell from the title of this post, I am VERY EXCITED :DD

As I mentioned in [Post #1](http://www.falcomaster.tech/2017/08/29/Post1/), I was going to investigate [p3](https://github.com/spxtr/p3), an existing template for bots. My goal was to find out how to communicate with Dolphin. If I could get p3 to work, I can move from there by looking through p3's code.

So, I needed to get p3 to work on my computer first. Which was the tough part.
<!-- more -->
I've never worked with Dolphin configuration before, so this process was extra confusing to me; the instructions online weren't clear, and there is no graphical interface for any of this (unless the computer terminal window counts as "graphical"). In case other people want to make bots as well in the future, I will now be providing detailed guidance (I'm assuming some knowledge of programming here, for the sake of concise instructions) into how I did this. Pictures included :)

First, I downloaded [p3](https://github.com/spxtr/p3) into a folder somewhere. I then created a pipe for p3. [Pipes](https://wiki.dolphin-emu.org/index.php?title=Pipe_Input) are a new addition to Dolphin that only work on UNIX systems (read: not Windows). To create a pipe, I typed the following commands in my terminal: `cd ~/.dolphin-emu`, `mkdir Pipes`, `cd Pipes`, and `mkfifo p3`. If you want to learn more of this, I highly recommend reading UNIX commands. I remember the first time I typed stuff in a terminal, I felt like a hacker :D

Second, I open my Dolphin emulator up. Go into the Controller Settings. Set one of the controllers to be Standard Controller. Also, at the bottom of this menu, hit the "Background Input" checkbox. This checkbox allows us to send outside input into Dolphin.

![](/Post3/step2.png)

Third, I move myself into `~/.dolphin-emu/Config` with the command `cd ~/.dolphin-emu/Config`, and look inside the files with the command `ls`. There **should** be a file called `GCPadNew.ini`. If it's not there, try going into the Controller Settings in the Dolphin emulator and hit the "Configuration" button next to the Standard Controller you created. There should be a drop-down menu asking for a device, and there should be something there you can select. The picture below shows the drop-menu. (To be honest, I don't know how to make `GCPadNew.ini` appear if it's not there, but this is my suggestion. No idea if this works; I was lucky enough to have it appear at some point :P )

![](/Post3/step3.png)

Fourth, go inside the p3 folder you made. The creator of this, [spxtr](https://github.com/spxtr), has graciously given us an example config we can use called `example_gc_profile.ini`. Copy the contents.

Fifth, open `GCPadNew.ini` in a text editor (I use Vim. Because why not. Don't get mad at me please). Paste the contents at the bottom; no need to delete anything (I think). But don't save yet! This is where I made my mistake. In your pasted contents, replace `[Profile]` with `GCPad3` if you put the Standard Controller to port 3. Change the "3" in "GCPAD3" to whatever port number you assigned the Standard Controller.

![](/Post3/step5.png)

So what's the point of all this? The first step was to create the pipe we need to communicate. The second step gives Dolphin an outlet for our commands to go through. The next three steps are installing spxtr's config file. If we didn't do those three steps, we would have to manually set the Standard Controller's inputs, which is extremely painful.

After all this, I ran p3 with spxtr's instructions, and presto!

![](/Post3/partyFox.png)

Now that this has finished, I can get to the fun parts. I can now dive deeper into the code for p3, and after that, design the neural nets to train Falcomaster! Stay tuned, everyone! <3
