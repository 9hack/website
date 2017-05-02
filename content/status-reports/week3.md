---
date: 2017-05-01T20:53:33-07:00
title: Week 3
---

## Group

**Weekly Status**

* Animations successfully implemented and working with our artist’s assets. 

* Shader render pipeline has become cleaner, making adding new shaders in the future more simple. 

* UI fixes with texture loading, added transparency, and added UI animations.

* Networking integrated with build phase: server confirmation when building constructs, and notifying all connected clients of grid updates.

* Beginning development of dungeon/exploration phase with player movement, collision detection.

* Continued progress on input layer abstraction between joystick input and game semantics.

* Researched and found a C++ library for playing audio that seems to be easy to use. Built a simple module to test out the library.

**Meeting Date**

Week 4: Saturday, April 29

**Group Morale**

The group seems to lack a sense of direction towards overall project architecture and how the final game will actually be implemented.  There seems to be a lack of direction due to the flat structure of the group, and perhaps a leadership/manager figure is necessary.  We plan to discuss this intensely during our Tuesday meeting.  Despite this, many are excited about the recent visual progress we have been making with the build phase.  Morale is shaky yet on the optimistic side — after all, everyone genuinely wants to see this project succeed.

Our group as a whole is also a bit worried about the overall progress of the game in that though we have a lot of code, we still seem to be in the building phase (without assets) whereas the meat of the game is in the dungeon phase and the minigames, both of which we limited progress on. For our meeting on Tuesday, we plan to collectively work towards getting an alpha out rather than focusing on perfecting existing modules.

**Screenshots**

![build-phase-gif](/img/screenshots/build-ui.gif)

<video width="640" autoplay controls loop>
  <source src="/img/screenshots/ui-anim.webm" type="video/webm">
</video>

![boy_multi_anim](/img/screenshots/boy_multi_anim.gif)

![boy_walk.gif](/img/screenshots/boy_walk.gif)


## Ethan

**Last Week’s Goals**

Discuss high-level architecture and begin delegating work as subunits.

**Completed Goals**

Unfortunately, our group wasn’t able to address this as much as I would have liked. It seems that our engine and its APIs are still too unstable for all of us to separately work with it. However, I did move the code towards a more client/server-oriented direction by multiplexing the main() method into different implementations. I also ended up working on translating raw controller input into more semantic context-aware events, and I hope to be done with that within a day or two.

**Unmet Goals**

As a team, we still need to discuss high-level architecture in detail. We have gone over it in broad detail, but I don’t feel comfortable with the level of mutual understanding we have of the game’s internal structure. I have been suggesting a more traditional group structure with a well-defined leader to unify our vision, but it seems for the most part our group is a bit nebulous.

**Next Week’s Goals**

Finish semantic input translation API, help Daniel get sound integrated, prototyping if time permits.

**What I Learned**

It’s quite hard to emplace any sort of change mid-way through a project. I haven’t needed to change many things about a project in the past, but there have been a few notable examples of this happening currently. While the group structuring I mentioned earlier is one such example, there are others like lack of commitment towards a particular art direction, and an attempt to change the medium through which our team communicates, which would have been much easier to set in place at the start. I feel like too much of the team was too eager to hit the ground running before we actually set up any team infrastructure and leading design principles. I wouldn’t be surprised if we would’ve decided to not repurpose a slightly ill-fitting engine, had we taken the time to actually do a cost/benefit analysis.

**Morale**

Still 6/10; I’m not as confident about this project as I am in others I’ve done due to the lack of internal team direction. It’s very hard to build any sort of velocity, since before you know it, another team member has made some large code change and you say to yourself, "oh, so we’re doing this instead now?" I just wish we had actually taken few solid hours at the very start to set the tone and direction of everything.

## Richard

**Last Week’s Goals**

My goal last week was to integrate networking into the existing build phase prototype.  

**Completed Goals**

I was successfully able to make the build phase rely on server-client networking.  Blocks that users request to build are first sent to the server as a request, and if it’s approved, the server notifies all clients that a block was build and to update their local grids.  Blocks built on each client will appear on all other clients’ games as well.

Since I was able to finish this early on in the week, I continued to work on refining the build phase and separate the game logic from the networking and UI.  I first set up a state machine consisting of game "Phases", which allowed for cleaner design overall.  I then worked on making the build UI modular (with a list of buildable constructs rather than hard-coded) and updated the UI.

**Unmet Goals**

Surprisingly, I have no unmet goals this week.  Granted, I did spend a considerable amount of time this week working on my tasks.  For next week, I will set more ambitious goals for myself.

**Next Week’s Goals**

For this coming week, I plan to work with Kavin to integrate networking into player movement so that players and see other players moving.  This would require the creation of some sort of Player objects that all clients have instances of.  This is dependent on movement being relatively finalized, and I imagine this will take up a majority of my work week.  In case I can’t progress or have free time, my stretch goal is to help out as much as I can on build phase gameplay and perhaps a lobby system.

**What I Learned**

As per Joshua’s suggestion, I learned quite a bit about how to implement finite state machines in code.  My initial assumption was to have some state variable with a large switch/case statement, but I learned about and used a class-based polymorphic state for Phases.

**Morale**

My morale this week is fairly high at 9/10.  A big factor was being able to accomplish my planned goals, plus a little more, but also starting to see the game’s visuals come together is encouraging.  Though we should definitely not make it a priority, I very much enjoy UI and visual design (basically making the game look pretty).  I’m a believer that it’s much more fun to work on a good-looking game than one that looks bad (in hindsight, this sounds quite obvious).

## Daniel

**Last Week’s Goals**

My goal last week was to do research about playing audio files in C++.

**Completed Goals**

I looked at a few C++ libraries and so far, the SFML library seems to be the most intuitive. It is cross-platform and easy to install (which is always nice, especially we have a ton of dependencies already). The API is relatively intuitive and easy to use too. The only caveat is that we will not be able to play mp3 files, only wav.

**Unmet Goals**

I attempted to compile our codebase on my machine, only to be met with a lot of dependency issues. I have a few more dependency issues to fix. On the bright side, it does not impede my work because right now what I am doing is modular. However, I need to get it to work soon because I will need to integrate the audio feature into our game.

**Next Week’s Goals**

My plans for next week are to do more research to get a better understanding of our current event system, which is based on Boost Signals. I plan to build a AudioManager prototype with an API that fits nicely with our game engine.

If I have extra time, I want to help with game logic development as well.

Also, once we have more art assets, I can start to brainstorm for the game music.

**What I Learned**

I learned how to play music files with C++, which was pretty cool.

**Morale**

Halfway through the quarter, I am feeling a little bit more uncertain now because it seems that our team has been stuck on graphics and codebase revamping for a while now. On the bright side, we have a barebones version of our server-client connection and one of our game phases partially implemented. I feel like as a team, we need to move towards producing an alpha version of the game with barebones graphics and put more focus on game logic rather than graphics.

## Christiane

**Last Week’s Goals**

Working on asset modeling, fixing playable character base model, as well as working on build phase UI art. Perhaps move level design/level modeling, depending on how the team wants to implement in level design. Determine if only need level designs as sketches and leave rendering for different program.

**Completed Goals**

Created textures for walls and floors to use in environment. Created two more assets while trying to refine character base. Collabed on UI design to look a bit more aesthetically pleasing. 

**Unmet Goals**

Did not finish base model, trying to match it to test model but making the mesh look better, but unable to be satisfied with the shapes. Also did not draw out level design yet since we still need game logic in play first.

**Next Week’s Goals**
Keep modeling assets for the game. Design levels to implement. Work on integrating assets into cohesive theme.

**What I Learned**

I learned that Blender is really a finicky monster sometimes. I also learned that we can’t just decide on modeling assets willy nilly without first deciding feasible game logic, since the coding side needs to be able to implement trap actions before actually going forward with making certain traps. 

**Morale**

Sleepy but excited to see it start to come together.

## Kavin

**Last Week’s Goals**

Last week my goal was to finish animation implementation.

**Completed Goals**

I created a prototype for player movement and interaction in the dungeon phase

**Unmet Goals**

I did not implement animation, it was handed off to Austin.

**Next Week’s Goals**

I need to add triggers to the player prototype as well as flesh out the player class itself.

**What I Learned**

I learned a bit more about the Bullet Physics library and what its weaknesses are. It shouldn’t affect our game that much though.

**Morale**

Morale is still relatively high. Being able to slowly branch off of the build phase is good since we can start gameplay logic.

## Austin

**Last Week’s Goals**

Finish up all the remaining functionality needed to complete the build phase prototype with the team, and then start focusing on creating the base classes and interfaces needed for having various types of game objects in the scene so that we may start moving towards the exploration phase.

**Completed Goals**

I ended up being in charge of getting animations loaded and working, which I was able to do successfully. Our asset loader now loads models and animations together, and so models can be attached multiple animations. This still needs to be tested with more complex models, but it seems to work for the models we currently have at least. In doing so, I cleaned up and worked with the rendering pipeline a bit to structure how models/game objects are done.

**Unmet Goals**

Didn’t get to focus as much on the exploration phase, but seems like Kavin got to do some work on that. After a few touches on it, I’ll try to get a good demo of the exploration done soon. Maybe like. Tonight. 

**Next Week’s Goals**

Give the team more direction on how the game will be structured, designed, and implemented. It seems like many people are getting lost on how the game will actually be made, and I feel like it just may be a lack of knowledge on the inner workings of the game engine itself. Since graphics seemed to end up including objects such as scenes/game objects/physics, the game mechanics portions of the game engine end up going more towards graphics. However, I feel that with some proper documentation and maybe some one-on-ones with everyone, it’d be easier to get everyone more comfortable with the mechanics and development of the final game.  More specifically, I’ll create both a game design doc, and a game mechanics roadmap, and then see how the team feels about it. I’ll move on to working on the minigame phase implementation afterwards. 

**What I Learned**

Communication is difficult. It takes up a lot of time to properly design and create a video game, and it becomes difficult to keep everyone on the same page. Even though we have our meetings and have these long discussions, there are still a lot of things in the game mechanics side that gets difficult to explain without having them actually work on it themselves. 

**Morale**

127%, as always. I have a very clear idea of how the progression of the game will be going, and even though it’s already getting close to the halfway mark, we have a lot of systems in place that will allow us to continue moving forward. I’m aware that a good part of it is overconfidence and naive thinking, however I have a lot of trust in the abilities of my entire team to pull  through and create something amazing. It also feels great being able to devote every single day to working on this project now that I am done with most of my other extracurricular stuff. 

## Joshua

**Last Week’s Goals**

A more concrete build phase instead of prototype. Resolve physics engine bug. Create more UI modules.

**Completed Goals**

This week was spent on revamping/refactoring our render pipeline (especially as pertains to the usage of shaders). I feel this was necessary to make graphics people’s lives easier down the line -- a cleaner and readily understandable and debuggable pipeline (though yet imperfect) replaced a relatively hacky one. As well, I resolved some issues we were having displaying images (textures) for our UI, and added transparency and animation capabilities to the UI system.

**Unmet Goals**

As you can see, my completed goals mismatch my intended goals. Richard sort of took the reins on fleshing out the build phase. The physics engine bug remains. UI modules were not created, but the UI system was improved upon.

**Next Week’s Goals**

Actually start building the game -- more specifically get the exploration phase up and running. I cannot express enough through these mere words how much I would like to move on to some tangible (by tangible I mean visible) stuff. I wish I could be more concrete with these goals instead of just nebulous inklings. I’ll be more precise: I want to see the ability for a player to move a model around in the map, with the camera centered upon the model -- and be able to see other players doing the same thing too.

**What I Learned**

Difficult to have a render pipeline work for every circumstance and still be clean and beautiful. Shaders need varying kinds of "uniform" data, and as different models can use different shaders, to create the proper abstractions for this seems impossible. 

**Morale**

Morale low because time passes too quickly for my comfort. Why is it week 5 already? I would like to see more visual progress on the game, but we sorely lack direction. Please instruct.
