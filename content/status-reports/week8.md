---
date: 2017-06-05T20:53:33-07:00
title: Week 8
---

## Group

**Weekly Status**

* Scoreboard UI

* Transitions UI

* Ice trap (slows players)

* Mimic chest trap with A* pathfinding AI

* "Slime Stampede" minigame preliminary development

* Sound effect development, original soundtrack in the works

* Spatial sound effects (i.e. sounds farther away sound quieter)

* More assets for player avatars, 1st/2nd/3rd/4th places, etc

* Dialog boxes

* In-game notification system

**Meeting Date**

Week 8: Sunday, June 5

**Group Morale**

Overall morale seems to be fairly high this week.  As we are nearing the deadline and completion (whichever comes first) for the game, there’s a rush to squeeze in as many cool features as we can.  However, there is a general consensus that we need to polish and refine our current game, and make it really fun to play, before exploring any of the extra features.  Our next week will consist of wrapping up existing features, fixing bugs, and polishing the core gameplay.  We seem to be on the optimistic side, and are excited to see what we can pull off by Friday.

**Screenshots**

![dialog](/img/screenshots/dialog.gif)

#### Dialog boxes
<br>


![notifications](/img/screenshots/notifications.png)

#### In-game notifications
<br>

<video width="640" autoplay controls loop>
  <source src="/videos/mimic_anim.mp4" type="video/mp4">
</video>

#### Mimic animation
<br>

## Ethan

**Last Week’s Goals**

Hook up dialog boxes to controls and provide a means to advance through script.

**Completed Goals**

I hooked up the dialog boxes, made them fully animated, and responsive to button presses. I also added a notification system and show notifications when another player reaches the goal. Finally, I added gold delta animations, to show how much gold you get or lose at any given time.

**Unmet Goals**

None.

**Next Week’s Goals**

Help Josh with transitions maybe. Depends on what needs to be done.

**What I Learned**

I learned that you need to be careful with dynamic allocation. I ran into a bug where animations would cause a segfault ONLY if the memory was freed. My "quick fix" ended up being just to not free the memory (I was originally using smart pointers that would do this for me).

I also have come to appreciate the nature of single-threaded event loops, as they grant you a lot of slack in terms of "asynchronous" logic.

**Morale**

7/10 as usual. We’re doing quite good but still haven’t nailed down an end-to-end product (results screen and transitions).

## Richard

**Last Week’s Goals**

My goals for this past week was to help with development of minigames, as well as refine core gameplay.

**Completed Goals**

I was able to help Kavin work on minigames, specifically the networking side and the phase/scene switching portions.  I was also able make several enhancements and bug fixes for the menu selection.

**Unmet Goals**

I wasn’t able to work much on gameplay refinement, which I wanted to.  I wanted to add smoother transitions in between phases and further refine build and dungeon phase, but I wasn’t able to.

**Next Week’s Goals**

This week, I plan to help everyone tie up loose ends, fix all bugs, and refine existing gameplay.  It’s a little too late for new feature development, so I really want to polish our existing game so it’s fun to play and demoable.

**What I Learned**

Didn’t learn too much new stuff this week.  However, due to many Bullet-related bugs, I’ve had to poke around and dive into that portion of our code.

**Morale**

Morale is at a 9/10 right now.  I’m finally done with my big event for my student org, so I plan to dedicate this entire week (as much as I can) to the game.  Looking forward to finishing strong!

## Daniel

**Last Week’s Goals**

Last week’s goal was to work on some traps, make a feature for spatial sound effects, and start on the original soundtrack.

**Completed Goals**

I released a pull request for spatial sounds: I developed an exponential decreasing function for the volume with respect to distance between objects. I also reworked how we play sound effects so we can play multiple of the same sound effect at the same time.

I also worked on some new sound effects. I came up with 8 motifs for our group to choose from for the soundtrack.

**Unmet Goals**

I was unable to continue making the wall spike trap because Austin said that rotation for the hitbox doesn’t seem to have a clean solution and the group wants me to focus more on the sounds at this point.

**Next Week’s Goals**

Merge the spatial sound feature into our main branch and create more sound effects to test it with (i.e. slime sounds). Also finish composing and producing our soundtrack. I also want to do tests to make sure that our sounds’ volumes are balanced.

**What I Learned**

I learned how to play multiple of the same sound effect of the same time by keeping a list of active sounds and swapping them out when they stop being active.

**Morale**

Morale is pretty high. The development workflow is going smoothly and the soundtracks are sounding nice. It’s also good to see that our whole game is coming together.

## Christiane

**Last Week’s Goals**

Get in final assets, making sure everything imports into the game properly. Perhaps do UV mapping for texturing models in order to help optimize? Design some UI icons and aesthetic

**Completed Goals**

Created player icons, logo, some menu text, sandma portraits 

**Unmet Goals**

Generating all model movements

**Next Week’s Goals**Finish model movements, calibrate character colors to work with new lighting, add more entities

**What I Learned**

video games are hard 

**Morale**

good, home stretch in sight

## Kavin

**Last Week’s Goals**

Try to get a working minigame phase.

**Completed Goals**

Richard and I were able to get a working minigame phase as well as the first minigame but there is a strange bug that occurs randomly. I also did small miscellaneous things such as mimic model/animation.

**Unmet Goals**

I suppose an unmet goal is a fully operational, bug-free minigame phase. However, I am still happy that we were able to get as far with it as we did.

**Next Week’s Goals**

The final stretch will include ironing out minigame phase bugs as well as implementing a couple more minigames for a variety of minigames to demo on Friday. I also will be on standby for any assistance on 3D asset creation.

**What I Learned**

Blender strikes again with issues of our model import code conflicting with exported model data from Blender. We think we have nailed down the most recent issue but I wouldn’t be surprised if another one pops up in the future.

**Morale**

Morale is still high and I’m excited to do the last week rush to the finish line. There’s a lot of polishing I would like to have done and I’ll try to help push us towards the end goal as much as I can.

## Austin

**Last Week’s Goals**

Make more complex traps, work on improving assets in the current state of the game, and aiding with the implementation of the scene changing system if needed.

**Completed Goals**

Made a new mimic trap that follows the player and attacks them, and also made an ice trap that slows player movement on collision. I also started working on the creation of a new type of dungeon map that would feel more stylistic for our game. 

**Unmet Goals**

We still need more assets for our game, and are currently still using temporary assets in many places.

**Next Week’s Goals**

Well, since this week is our final week. Next goal is to complete our game and have it in a state that we will be proud of. For me, this will include helping everyone out with their subsystems, gameplay balancing, and more content for the game. 

**What I Learned**

Making video games is hard, but fun and rewarding. There are ups and downs, and many struggles. But overall, we’re creating something new from scratch that will be fun for others to enjoy.

**Morale**

Ready to give it my all this week. Let’s make some miracles happen. 

## Joshua

**Last Week’s Goals**

Main menu, more efficient text rendering. Scene transition effects. More instanced rendering on things like essences.

**Completed Goals**

More efficient text rendering, but turns out we don't need it. Did scene transition effects via ui. Additionally tweaked scoreboard ui.

**Unmet Goals**

No main menu because it's just going to be an image. Turns out we don't​ need instanced rendering for essences.

**Next Week’s Goals**

Finish up everything.

**What I Learned**

Game development and game engine development are hard.

**Morale**

7/10.
