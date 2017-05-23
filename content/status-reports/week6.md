---
date: 2017-05-22T20:53:33-07:00
title: Week 6
---

## Group

**Weekly Status**

* Sound effects feature added to audio manager

* UI: previews of constructs currently being built, game timer

* Increased compilation speed manyfold via precompiled headers

* Gameplay: purchasing constructs, end goal action

* Content: spike trap, currency, new players, dream essence (dropped on damage)

**Meeting Date**

Week 6: Sunday 5/21

**Group Morale**

Morale is generally high.  Overall, everyone is fairly satisfied with the progress we’ve made in the past week.  However, with the final few weeks remaining, we know there is still lots of be done, and we will continue to push forward.

**Screenshots**

![essence party](/img/screenshots/essence_party.gif)

#### Dropping dream essences upon taking damage
<br>

<iframe width="640" height="360" src="https://www.youtube.com/embed/bMi3ak4WXCo?rel=0" frameborder="0" allowfullscreen></iframe>

#### Bigger map, construct purchasing, end goal
<br>

## Ethan

**Last Week’s Goals**

Fully implement timed phase changes with a graphical timer. Stretch goal: work on a results screen of sorts.

**Completed Goals**

I was able to complete the graphical timed phase changes. Since the results screen and other "phases" involve a lot of work spanning multiple files, we felt that we should wait for things to settle down a bit before getting started on it. In the meantime, I worked on some infrastructure for our currency and collectible system.

**Unmet Goals**

No unmet goals, besides the stretch goal.

**Next Week’s Goals**

Depends on what Richard thinks will be good for me to work on. I seem to be the resident expert on gold-related stuff now, so maybe more things involving that.

**What I Learned**

Even though I tell others to do smaller PRs frequently, I too am guilty of bundling multiple unrelated things into one PR. I should really do each one separately, because this week I ran into a lot of merge conflicts. Had I done each feature as a separate PR, there would be a lot less conflicts to sort out and I would know much more easily what is safe to merge or get rid of.

**Morale**

The usual 7.5/10. We’re making good progress, but we’re still behind.

## Richard

**Last Week’s Goals**

Last week, my goal was to integrate networking functionality for various gameplay features.

**Completed Goals**

I was able to help out a lot on the networking side of various gameplay features, such as: player reconnection, reaching the goal to end dungeon phase, per-player spawn points, start-button to signal ready, purchasing constructs, closing chests, and so on.

**Unmet Goals**

I don’t have any unmet goals, since my goal for this week was just a general goal for doing what needed to be done.

**Next Week’s Goals**

My goal next week is to continue helping to integrate networking into my teammates’ features, and also start working on a basic menu with character selection.  I also plan to help out with minigames if Austin gets started on it.

**What I Learned**

I learned, once again, that our team is 10x more productive when we’re working together.  As a result of our "hackathon meeting", where we got together to work on the project, we got a lot of features done and pull requests merged in.  It’s a lot easier to ask people questions and get things merged into master when everyone’s together.

**Morale**

I’ll say this week’s at an 8.5/10.  After seeing our work this past week, we definitely have the potential to get a lot done.  It’s just a matter of continuing to push forward in these final few weeks.

## Daniel

**Last Week’s Goals**

Last weeks goals was to incorporate sound effects into the audio manager.

**Completed Goals**

I merged the audio manager into our code base and also did a pull request Richard put up for a feature to mute music with a button. I was also able to incorporate sound effects into the audio manager, which differs from music in that we load the sounds beforehand into memory.

**Unmet Goals**

The goals of this week was met.

**Next Week’s Goals**

Next week’s goals are to make more sound effects and to help the other members get familiar with using the audio manager to play sounds. I might also help Austin with making traps and assets.

**What I Learned**

I learned to be more familiar with the workflow of working on a shared code base. I also learned how to use the SFML library better now.

**Morale**

Morale is a bit higher this week because I was able to get work done without too much blocks. I ran into memory problems with the SFML library which got me stuck for a few hours, but I managed to resolve it. My laptop was slow in compiling and running the game so I set up my desktop for the project and things are going way smoother.

## Christiane

**Last Week’s Goals**

Come up with logo and finish in-game shop. Create a bunch of random items to be used in the game.

**Completed Goals**

Created new character, fixed animations on messed up models and created more animations for interaction.

**Unmet Goals**

Did not finish shop, only began drafting logo and UI designs.

**Next Week’s Goals**Finalize logo, finish remaining characters,  add in other assets needed. New textures to make stages look nicer.

**What I Learned**

I learned a permanent fix for the wonky models so now I know how to adjust it accordingly in Blender. I also found out that the colors in blender do not look the same when implemented into the game, so adjusted colors accordingly.

**Morale**

Home stretch excitement but nervous

## Kavin

**Last Week’s Goals**

Add more connectivity to the game’s separate phases.

**Completed Goals**

I added more elements to the game in order to make flow better visually (a warp animation for reaching the goal, overworld camera after you reach the goal) as well as logic for game flow (gamestate flags for dungeon phase). Also small things like D-pad control for building.

**Unmet Goals**

No major unmet goals for this week

**Next Week’s Goals**

Add logic for a beginning menu phase before the game starts.

**What I Learned**

I learned a bit more about how the game flows in terms of server/client interaction. 

**Morale**

Morale is pretty good, a lot of advances this week were visual so progress felt more satisfying because I could directly see the work I’ve done.

## Austin

**Last Week’s Goals**

Focus on getting the functionality for the dungeon phase completed, and begin moving towards the mini-game phase. 

**Completed Goals**

Got our first trap integrated with the networking side. Created a visual representation for currency in the dungeon phase, and worked on the logic for damaging and stealing. Currently working on getting moving traps integrated into the system.

**Unmet Goals**

The mini-game phase remains untouched.

**Next Week’s Goals**

Provide a good-enough foundation for traps and other structures in the game, hopefully allowing other members in the project to add their own trap ideas in a simpler manner. Then start integrating a basic mini-game phase and experimenting on whether or not the phase is still viable for our final demo. 

**What I Learned**

I learned a lot this week about how to work with the networking side of the project. I’ve come to believe that our biggest downfall was our initial implementation of the game without considering the networking side, which led to multiple weeks being focused on simply translating the game engine to work with the network. Realizing this made me want to get a better grasp of the networking code, so that we can no longer have to worry about possibly unusable code when combining the network and graphics together.

**Morale**

We have less than three more weeks on this project. Working on this game was some of the most fun and enriching experiences in game dev that I have had. Although we are far behind in where I would want our project to stand, I’ve learned a lot through the journey we’ve taken here and can see the skills I’ve learned being useful as I expand my career into game dev. I will continue devoting as much as I can to make this project as successful as it possibly can. 

## Joshua

**Last Week’s Goals**

Selection previews of grid constructs, main menu, ui clock, ui score display/leaderboard. UI performance maybe.

**Completed Goals**

Got selection previews in, with green transparent version of the models to indicate selection. Was not able to get to main menu and leaderboard UIs, but was able to get a UI clock going along with various UI improvements (excluding UI performance, which we have somewhat ruled irrelevant at the moment). Aside from these completed goals, I also increased the compilation speed in Visual Studio manyfold by using precompiled headers. Should have done this much earlier to speed up iteration cycles.

**Unmet Goals**

Unable to get main menu and other menus, as well as some leaderboard UI up. Should be relatively easy given what we have currently in place.

**Next Week’s Goals**

Finish up menus like I was supposed to do.  Along with leaderboard and gold UIs. Maybe dialogue boxes for what we want to do. UI animations as well. Everything UI, and then secondarily help others with actual gameplay.

**What I Learned**

Should have really pinned down and fixed the compilation speed issues we were having earlier. It actually played a huge role in demoralizing the team because of how slow development can get with slow compilation.

**Morale**

High, given that I can test small code changes (including header changes) without having to wait 7 decades.
