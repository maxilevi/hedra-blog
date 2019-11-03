---
layout: post
title:  "Weekly Update #1: First entry!"
date:   2019-10-27
author: Zaphyk
---
This is going to be the first post of many more that I am going to be writing weekly in order to showcase all progress that is being done in Project Hedra. My intention is to release one every Sunday, I'll try to showcase several pictures and keep them short so it's more visual to the reader :) Let's start:

## Art

On the art side a lot has been going on, afro has been working on getting the new bosses and critters off the ground. Below are some pictures and GIF of the new stuff:

The new boss "Azathul" resting in zen position

![](/assets/img/azathul_zen.jpg)

When the boss is waken up or alerted this animation is played:

![](/assets/img/bossshroom.gif)

Azathul's ready-to-combat stance

![](/assets/img/bossshroom_done.jpg)

Progress has also been made towards new minions that sorround this new boss. Here is a new animation for the minion that was briefly [showcased on the previous post](https://blog.projecthedra.com/2019/10/17/art-update-2.html)

![](/assets/img/agro_biped.gif)

Afro also designed & conceptualized a very cool and distinct attack for it.

![](/assets/img/longarm.jpg)

Here is a GIF showing it in action:

![](/assets/img/powerattack_shroomguard.gif)

Knockdown animations were also added:

![](/assets/img/bipedknockdownloop.gif)

And different attacks too

![](/assets/img/stabguarded.gif)

## Development

On the technical side i've been working on doing some improvements on the game engine. Previously the game was using [OpenTK](https://github.com/opentk/opentk) as a windowing library (it abstracted interaction with the Windows API and OpenGL context creation) this worked OK on most systems but it contained some obscure bugs mostly due to it not being maintained anymore. This among other reason I decided to move the game to a more stable and tested library, [GLFW](https://www.glfw.org/) this decision will hopefully help us avoid more technical issues in the future.

Because the game is written in C# this required me to use a binding for GLFW, this lead me to incorporate [Silk.NET](https://github.com/Ultz/Silk.NET) into the game, which basically is a C# wrapper around OpenGL, GLFW and OpenAL. This change required me to rewrite several parts of the code but in the end I think it's worth it :) 

I also worked on creating [this](http://blog.projecthedra.com) new cool blog that will serve as a platform for showcasing & sharing the development in the game.

Several other things have been done but in order to keep things short I'll cut it here. If you want to see more, you should check out the [discord](https://discord.gg/AEC4Uab)

That's all!
