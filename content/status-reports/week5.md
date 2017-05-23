---
date: 2017-05-15T20:53:33-07:00
title: Week 5
---

## **Group**

**Weekly Status**

* Collisions and interactions over the network

* End goal placement

* New models with better animations created

* AudioManager implemented. We can play music in our game now :)

* Instanced rendering - improved frame rate twenty-fold

* Player flickers to indicate being damaged

* Simple spike trap working

**Meeting Date**

Week 5: Saturday, May 13

Monday, May 15

**Group Morale**

Morale this week is fairly high overall.  We’re making good progress, but since we were unable to complete the overall gameplay, we feel a bit disappointed and slightly behind.  That said, our graphics and visuals look very promising, and many pieces are coming together.  Our performance (framerate) optimization means that development workflow will be more streamlined.  We’re optimistic and determined to continue creating the game.

**Screenshots**

<iframe src='https://gfycat.com/ifr/AncientNegativeGopher' frameborder='0' scrolling='no' allowfullscreen width='640' height='360'></iframe>

#### Goal placement and animation
<br>

<iframe src='https://gfycat.com/ifr/AcceptableSophisticatedGroundhog' frameborder='0' scrolling='no' allowfullscreen width='640' height='448'></iframe>

#### New character, on-hit animation, object interaction
<br>

![big grid](/img/screenshots/big-grid.png)

#### A very large grid (and very high FPS!)
<br>

![debug draw](/img/screenshots/debug-draw.jpg)

#### Game object wireframes for debugging
<br>


## **Ethan**

**Last Week’s Goals**

Fix game loop bottleneck, look into the "catch up" game loop.

**Completed Goals**

I was able to identify and fix the game loop bottleneck by using the "catch up" game loop pattern; this allows for some leeway in lag spikes and sacrifices a bit of FPS to update the game to the state where it should be. I also got a start on implementing timers that will switch from phase to phase, but I had to scrap most of my work due to conflicts with other branches. However, I have the basic idea down and have dealt with the weird scoping and compilation issues, so replicating it once master is stable again should be no big deal.

**Unmet Goals**

No unmet goals because I only really set the loop bottleneck goal.

**Next Week’s Goals**

Fully implement timed phase changes with a graphical timer. Stretch goal: work on a results screen of sorts.

**What I Learned**

I learned that you have to be very careful with references in C++, because they are not as safe as I initially thought. There will be no warning if you use a reference to something on the stack and it gets popped off. I found out the hard way when I kept getting weird values for the number of seconds I was passing to my timer callback. To ensure non-stack-dependent preservation of values, one must use a *mutable* lambda to preserve variables captured by equality as state that exists for the lifetime of the lambda.

**Morale**

7/10 this week because I got sick, and some slight disappointment with the architectural state of the codebase. However, I know that we’ve been doing our best, and the state of the codebase is on the shoulders of every member. I basically have to make the best plays with the cards dealt to me.

## **Richard**

**Last Week’s Goals**

My goals last week were to implement collisions and interactions over the network.  If time permitted, I would help with basic gameflow.

**Completed Goals**

I was able to complete my goals of getting collisions and interactions over the network.  However, since I became busy with some student org matters, I wasn’t able to complete my additional goal of helping on gameflow very much.  Although, I helped work on goal placement over the network.

**Unmet Goals**

As mentioned above, I was unable to help much with overall gameplay.  This was due to a mix of me being busy, as well as waiting on a pull request to reviewed and merged in.  It’s all good now though.

**Next Week’s Goals**

For next week, I plan to continue working feverishly on core gameplay, and attaching networking integration to my team members’ new features.  In particular, sending more information about the game state over the network, having the server control the flow and state of the game, etc.

**What I Learned**

I didn’t really learn much this week regarding what I’m currently working on, but I learned a bit from Joshua about the performance optimizations he worked on.  Though I’m not too well-versed in graphics, it was pretty neat learning about how the GPU renders objects (and how we can work around this).

**Morale**

Morale is about the same as last week, at about 7/10.  Slightly disappointed that I wasn’t able to finish my stretch goals, and anxious that we only have a couple weeks left of development.  However, I’m pretty excited about how our game is turning out both graphically and gameplay-wise.

## **Daniel**

**Last Week’s Goals**

Integrate music-playing capabilities to our game.

**Completed Goals**

I created an AudioManager that manages (background) music files. It can be extended to sound effects. We can now play different music in different phases of the game. I submitted my code for a pull request.

**Unmet Goals**

I did not get to creating the soundtrack, but it’s something that I will get to next week. I also did not implement the sound effects part of the AudioManager, but once the pull request gets approved, it shouldn’t be too hard to implement.

**Next Week’s Goals**

I plan to work on the unmet goals. If those go smoothly, perhaps help out the other members with different aspects of the project.

**What I Learned**

I learned about C++ lambda functions while implementing AudioManager. I also learned how to use Boost Signals correctly. I became more familiar with Microsoft VS and git/pull requests.

**Morale**

Moral is pretty good now I have my pull request up and things seem to be working quite smoothly. I am glad I am making progress and contributing to our codebase. As the deadline draws near, I’m starting to be a little bit anxious since we don’t have basic gameplay up yet, but I know we are all trying our very best and that we have a lot of the pieces of the puzzle.

## **Christiane**

**Last Week’s Goals**

Finish up existing assets that need to be created. Brainstorm up ideas for game logo/mascot to help pull game theme together

**Completed Goals**

Finished creating the base model and generated two completed playable characters to be used into the game. Animation and models imported correctly into the game.

**Unmet Goals**

Have not yet created game logo; considering naming for game. Need at least two more playable characters modeled for a completed roster of 4, and aiming to keep making various characters for a variety. Have not yet created the random items to be utilized in the mini-game.

**Next Week’s Goals**Come up with logo and finish in-game shop. Create a bunch of random items to be used in the game.

**What I Learned**

I learned (as with every week) just how much of a headache Blender can be. I found out how to remedy some issues I ran into, such as models skewing once animation was exported and now have a seamless base model to work with.

**Morale**

High when seeing game assets imported into the game; low when Blender acts up and I don’t know what the problem is because I’m not entirely proficient in all of the program’s shortcuts/features/options that could mess up the model if not carefully handled.

## **Kavin**

**Last Week’s Goals**

Implement goal functionality

**Completed Goals**

Created a rough prototype of spikes that was handed off to Austin. Got placement of the goal working.

**Unmet Goals**

The game flow isn’t complete yet but I’ll see where the night takes me.

**Next Week’s Goals**

Add more connective tissue to the game (loading screens, menus) so that game flow is there both graphically and in functionality.

**What I Learned**

Didn’t learn too much, I suppose I was able to brush up on Blender with some tweaks to models/animations.

**Morale**

Still the same as always, there hasn’t been any major downers to change it.

## **Austin**

**Last Week’s Goals**

Finish up the dungeon phase and make sure to flesh it out before we can move on to the minigame phase. Specifically, work on the implementation of traps, player parameters, and more efficient rendering

**Completed Goals**

Worked out traps a bit more, getting a simple spike trap to function. Helped Joshua a bit regarding instanced rendering to improve game performance. 

**Unmet Goals**

The main parameter for the player is currency, which is still in the middle of being integrated into the game. The dungeon phase is getting closer to being finished, but still requires some more work. 

**Next Week’s Goals**

The dungeon phase took longer than expected, but the basis for it will be completed soon. What still needs to be added is the notion of currency (which is almost complete), a countdown timer, and a proper portal for transitioning to the waiting room. Once completed, I will be focusing more on the minigame system.

**What I Learned**

I enjoy making games. So even when I know I have deadlines to meet, or do not have as enough time to work as I hope, I should still enjoy my work along the way. 

**Morale**

Always 100%. I know that we still have a lot of work to do, but I am hoping that everyone on the team is as ready as me to begin working as hard as they can to meet our goals. 

## **Joshua**

**Last Week’s Goals**

Fix performance (read: framerate) issues via instanced rendering. Collision masks for powerful control over which objects can collide with each other. Integrate the Bullet debug drawer.

**Completed Goals**

Implemented instanced rendering which improved our framerate literally twentyfold (with uncapped, no vsync).

**Unmet Goals**

I did not get to collision masks. As for the Bullet debug drawer, Austin took care of that.

**Next Week’s Goals**

Redo selection of grid constructs (with instanced rendering, cannot change individual tile parameters). Work on main menu and misc menus, ui time, ui score display/ranking whatnot. Maybe address ui performance when it comes to framerate.

**What I Learned**

Instanced rendering is relatively new to OpenGL (2010, version 3.3+) and one of our team member’s computer does not have support for the OpenGL features I used (actually just a specific one, glVertexAttribDivisor). We will make do.

**Morale**

Morale is a solid 7/10. 
