---
date: 2017-05-29T20:53:33-07:00
title: Week 7
---

## Group

**Weekly Status**

* Leaderboard and gold UIs

* Gamma correction, HDR, bloom

* Moving traps (slimes) and projectile traps (arrow)

* Construct rotations

* Controller legend and dialog boxes

* Player avatar selection

* Scene switching

* Beginning development of minigames

**Meeting Date**

Week 7: Friday, May 26

**Group Morale**

Group morale is decent, but slightly strained due to the increasingly close deadline.  Our team is starting to feel a bit bogged down due to commitments to other classes or activities, and as such, progress towards a full game experience is not quite complete (but nearly finished).  However, our group is still determined to finish strong and put our best effort into these remaining weeks.

**Screenshots**

![dialog boxes](/img/screenshots/dialog-boxes.png)

#### Dialog boxes
<br>

![leaderboard](/img/screenshots/leader.png)

#### Leaderboard UI
<br>

![arrow trap](/img/screenshots/arrow_trap.gif)

#### Arrow trap
<br>

![slimes](/img/screenshots/slimes-crop.png)

#### Slimes
<br>

<iframe width="640" height="360" src="https://www.youtube.com/embed/TVV_v4dA6MY?rel=0" frameborder="0" allowfullscreen></iframe>

#### Slime party
<br>

<iframe width="640" height="360" src="https://www.youtube.com/embed/lM280g5piHQ?rel=0" frameborder="0" allowfullscreen></iframe>

#### Gameplay
<br>

## Ethan

**Last Week’s Goals**

Whatever people wanted me to work on.

**Completed Goals**

Controller legend UI, dialog boxes WIP.

**Unmet Goals**

None.

**Next Week’s Goals**

Hook up dialog boxes to controls and provide a means to advance through script.

**What I Learned**

We took a peek at what some other groups were doing, and I really regret not using more libraries/frameworks. We’re reinventing the wheel with our UI implementation. It’s a bit too late to stop now though, I suppose...

**Morale**

7/10, since we still don’t have an end-to-end game yet, i.e. we couldn’t sit two random strangers down to play our game and give feedback on the experience because we don’t have a whole experience.

## Richard

**Last Week’s Goals**

My goals last week were to start on character selection of the menu phase, integrate networking into new game features, and help with minigame development.

**Completed Goals**

I was able to implement character selection (avatar switching).  I also implemented scene switching so that we could transition from the start scene to the main scene (build and dungeon phases).  I also did a lot of protobuf work to make it easier for Austin’s projectile traps to work well.

**Unmet Goals**

I started doing minigame development with Kavin, though we are definitely in the initial exploration phases.  We’re working through some initial kinks but overall prospects seem good.  If we’re unable to set up a basic minigame by mid-week, we’ll probably scrap the minigames and focus dev resources on refining the core game.

**Next Week’s Goals**

This week, my goal is to help with development of minigames.  If that doesn’t work out, I’ll help with further refining the menu phase as well as core gameplay.

**What I Learned**

Didn’t learn too much new things this week, but because I did a lot more graphics-related tasks this week, I got a much better insight into how things work in that world.

**Morale**

Morale is slightly lower at a 7/10, mostly because I’ve been tied up with some extracurricular things.  Hoping to work a lot on the project in these few remaining weeks.  However, pretty happy with all the progress we’re making; the new traps are looking really cool.

## Daniel

**Last Week’s Goals**

Finalize sound effects and start working on traps.

**Completed Goals**

I pushed the changes to the AudioManager, adding the feature of enabling sound effects; I put up the workflow for adding a sound effect to Slack for reference.

I started working on a wall spike trap with Austin’s help.

I made some extra sound effects. I also started to work on a requested feature that allow sound effects to play with different volumes with respect to distance.

**Unmet Goals**

Though I was able to get the model and hitbox working for my trap, with the current rotation scheme we have, we aren’t able to rotate hitboxes. Austin and I are looking into that at the moment.

**Next Week’s Goals**

I want to get the new sound effects feature out as soon as possible and make some new sound effects. I also want to complete the trap and start working on new ones.

**What I Learned**

I learned about our game engine, i.e. game objects and game constructs, and the workflow to build a trap.

**Morale**

Though there were some hiccups I ran into while revising the AudioManager as per the Ethan’s comments in the pull request, I was able to eventually resolve it and make it work satisfyingly. Working on traps have been fun too, despite the sheer amount of code I have to go through since I had been working on different aspects of our game.

## Christiane

**Last Week’s Goals**

Finalize logo, finish remaining characters, add in other assets needed. New textures to make stages look nicer.

**Completed Goals**

Fixing up animations on character models. Made different designs for game logo that will decide what the menu theme will look like; waiting for input on more design ideas for a solid logo. Making new model to change with slime placeholder.

**Unmet Goals**

Not finalized logo so no actual menu aesthetic look yet. Need at least one more character model

**Next Week’s Goals**Get in final assets, making sure everything imports into the game properly. Perhaps do UV mapping for texturing models in order to help optimize? Need to look into that.

**What I Learned**

Not much new content learned per se, however found out there was a small bug with models in a particular animation even though the model looks fine in Open3Mod. Discussed with Austin; might be a coding flaw.

**Morale**

6.5/10 Wasn’t able to get exactly what I wanted finished done because of bulk of other classwork

## Kavin

**Last Week’s Goals**

Create initial logic for a start phase/menu before the actual game begins.

**Completed Goals**

Various things got implemented such as dungeon rewards for finding the exit, construct rotation since we have directional constructs now, added a light to the goal, a rough start on a start scene and character selection,  and an arrow trap model/animation

**Unmet Goals**

I would have liked for the start menu to be more polished but at least primary functionality is present.

**Next Week’s Goals**

I will be working with Richard to see if we can reach our stretch goal of minigames, if we can’t then we will shift focus to help other members of the team and general polish of what we already have.

**What I Learned**

Blender exports models in a strange way when using different material colors. We have to switch to texturing for more detailed models.

**Morale**

Same as always however I have some trepidation with the deadline coming ever closer.

## Austin

**Last Week’s Goals**

Provide a good-enough foundation for traps and other structures in the game, hopefully allowing other members in the project to add their own trap ideas in a simpler manner. Then start integrating a basic mini-game phase and experimenting on whether or not the phase is still viable for our final demo.

**Completed Goals**

I got both moving traps and projectile traps working. In doing so, I created a much more structured method for organizing and creating new constructs in the dungeon phase.

**Unmet Goals**

I still would like to work on more complex traps for the dungeon phase. I also handed off working on the mini-game phase to other members in the project, and instead have been focusing on making traps in the dungeon phase.

**Next Week’s Goals**

Make more complex traps, work on improving assets in the current state of the game, and aiding with the implementation of the scene changing system if needed.

**What I Learned**

You can put as many "hours" into working on a project as you want, but the only numbers that really matter are efficiency and morale. 

**Morale**

I am quite disappointed with the progress we’ve made in the past week (relative to the amount of hours we’ve put into working together), and a lot of it was due to issues in our code structure that we have over-looked in our initial development. The issues themselves may have been small, but facing them seemed to affect our progress in more ways than one. Nevertheless, we have less than two weeks left before the final day. I understand that our project is messy, but we have goals to achieve that requires everything we’ve got. 

## Joshua

**Last Week’s Goals**

Do UI menus. Along with leaderboard and gold UIs. Dialogue boxes. UI animations as well.

**Completed Goals**

Finished leaderboard and gold UIs. Gamma correction, HDR, and bloom. Fixed animations not playing within the shadows of objects. Examined framerate issues.

**Unmet Goals**

Main menu, basically. Dialogue boxes Ethan has taken over. Did not get to UI animations, but should be simple to implement.

**Next Week’s Goals**

Main menu, more efficient text rendering. Scene transition effects. More instanced rendering on things like essences.

**What I Learned**

Learned about advanced lighting techniques (HDR, bloom), as well as the necessity of gamma correction.

**Morale**

Around a 7/10.
