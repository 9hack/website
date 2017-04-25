---
date: 2017-04-24T20:53:33-07:00
title: Week 2
---

## Group

**Weekly Status**

- Refactored vast majority of codebase

- Event system using boost::signals2

- UI framework

- Network: Connect using Asio and serialize using Protobuf

- List of game assets for the dungeon phase (with pseudocode)

**Meeting Date**

Week 3: Saturday, April 22

Week 3: Monday, April 24

Richard and Daniel met up to go over our network protocol and Protobuf. They discussed how the game logic can be added.

**Group Morale**

The group’s morale seems to be pretty average as we have been able to work a lot on the foundations of the project, but have not made any significant visual progress.

**Screenshots**

![week 2 ui screenshot](/img/screenshots/week2.png)

![character model 1](/img/concept-art/characters/model1.gif)

![character model 2](/img/concept-art/characters/model2.gif)

## Ethan

**Last Week’s Goals**

My goals were to have a fully functioning joypad input abstraction layer, make headway on the networking stack, and get some unit testing in place.

**Completed Goals**

I was able to develop an event-oriented joypad input API, and refactor several other areas of our codebase to use the same event architecture. I also worked with Richard to incorporate protobufs as our serialization strategy, which worked out splendidly.

**Unmet Goals**

I was unable to get any progress on unit testing, mostly because the lack of testable items brings little merit to investigating testing solutions. Given the presentation-focused nature of our product, I think it is reasonable to not incorporate tests until it becomes apparent that regressions are happening on a regular basis. Reliability and security are of little concern due to the one-off nature of the project.

**Next Week’s Goals**

Discuss high-level architecture and begin delegating work as subunits.

**What I Learned**

Kavin and I spent a large chunk of this week refactoring code from the old codebase we were intending to build upon. It became apparent to us over time that working with this codebase wasn’t pleasant; it wasn’t designed for a game. It was designed for a tech demo, and this became evident upon seeing all the singletons and debug flags strewn about the code. Not to mention, a lack of decoupling. This is okay for a tech demo, but for a large application being worked on by a large team, it makes it nigh impossible to get anything done without combing through a large portion of the codebase. Lesson learned: don’t hastily assume tangentially related code can be easily extended for a different purpose.

**Morale**

I haven’t run into any more OS-specific issues this week, so my morale has improved a bit. However, I still would say it’s at only about 6/10. I’ve been having some disagreements with the graphics team about what level of abstraction is acceptable; it’s not a matter of being able to pick up graphics, as much as it is a matter of reducing cognitive load when dealing with business logic. We also haven’t had any substantial discussions about high-level architecture, which concerns me. We have a lot of bits and pieces developed, but I feel as though no one really knows how they fit into the puzzle as a whole. Hopefully we can have some discussion about this and bring a sense of direction to the project.

## Richard

**Last Week’s Goals**

My goals this past week were to further refine the networking code and work on initial protocol design and integration. If time permitted, I would work on game logic. 

**Completed Goals**

I was able to make substantial improvements to the networking code in terms of design and stability. I also integrated Google's protocol buffer library for serialization and deserialization of message structures, which will make it easy to send custom messages.

**Unmet Goals**

Even though it was a stretch goal, I was unable to meet my goal of working on the game logic.  The time and resources spent on refactoring prevented us from being to do further gameplay development.  

**Next Week’s Goals**

For this coming week, now that the networking code is essentially finished, I plan to continue integrating networking into the build phase.  The target is to have the build phase prototype done early this week, which will allow me to add multiplayer functionality.

**What I Learned**

Prior to this week, I hadn’t heard of protocol buffers, so learning about them and how to use them was really interesting.  Other than that, I researched more about game architecture and design, so learning about those was insightful as well.

**Morale**

Now that I’m no longer sick, and after having made significant progress this week, I’d rate my morale at a healthy 8/10.  I’m still eagerly awaiting our integration of the build phase, so without much visual progress to be able to show off, my morale is hindered.  But I’m excited to see our hard work on our respective components come together.

## Daniel

**Last Week’s Goals**

Last week, I was in charge of producing a list of game assets (hazards, structures, items) for our dungeon phase. As part of the networking team, we needed to decide what tools to use to connect the server and the client and develop our own protocol.

**Completed Goals**

I was able to create a list of game assets with their high level description, (programming-wise) what we need, how it can improve the fun factor of the dungeon phase, and a lower level step-by-step pseudocode.

The networking team decided on sticking with the Boost Asio Library to do the TCP connection. We also used Protobuf to serialize our objects to send as messages across the network. Even though I did not write the code for it, Richard  briefed me on our protocol and I now have an understanding of our network protocol.

On the side, I also drew two concept arts for how our dungeon phase can look like.

**Unmet Goals**

Due to my student org activities, I was unable to do coding for the networking portion. Also due to the nature of the network code, it is less messy and confusing for one person to do it and for everyone to discuss after.

**Next Week’s Goals**

Now that we have the network protocol set up, next week we will focus more on game logic. We need to decide how the server is going to keep track of the state of the world and also event-handling logic. To do that, I will need to have Visual Studios and the environment set up on my other laptop.

I will also talk to Christiane about her art concept and try to come up with motifs and idea for our game music. This is a nice to have so it is of lower priority.

**What I Learned**

I learned how hard it is to write general pseudocode when all the "code" you have is “collision detection” and “tile detection.” Hopefully my pseudocode is going to be useful when we actually make the game.

I also learned a lot about Protobuf thanks to Richard’s debriefing. It is definitely a serialising technique that will suite our needs well without introducing too many dependency issues.

**Morale**

The team is very understanding when it comes to working around each other’s schedules; this makes working with each other less stressful and more enjoyable. We seem to be making decent and steady progress. Ethan and Kavin are working hard to refactor our code base, but once the dirty work is done, it should be smoother from here on.

## Christiane

**Last Week’s Goals**

Create refined character design and more level design, as well as starting to model assets to give to the team to implement into the game.

**Completed Goals**

Modeled a test character and did a very basic rig and animation of the character in Blender. Got a better aesthetic sense of what graphics will look like in completed game. 

**Unmet Goals**

Level designing; need to discuss with those working on this side of the project for the best way to integrate into the game. 

**Next Week’s Goals**Working on asset modeling, fixing playable character base model, as well as working on build phase UI art. Perhaps move level design/level modeling, depending on how the team wants to implement in level design. Determine if only need level designs as sketches and leave rendering for different program.

**What I Learned**

Since only using Blender about once or twice over a year ago, I reviewed how to use it again. However, this time around I familiarized myself a little more with shortcuts as well as streamlining the process in character modeling versus basic shape manipulation in order to get a more symmetrical model. I also learned how to do rigging and animation within Blender in order to demonstrate some model movements that can be done. 

**Morale**

Medium to high morale; Blender is frustrating as sometimes things get finicky when modeling and completely skews the model that is being worked on. Sometimes wireframe acts up and is hard to remedy without trying to cheat and hide through coloring. Otherwise, seeing finished product increases my morale.

## Kavin

**Last Week’s Goals**

My main goal last week was to get an animation system working in the engine.

**Completed Goals**

I refactored the rendering pipeline for our engine and also did general refactoring.

**Unmet Goals**

I wasn’t able to work on the animation functionality due to the refactoring that was needed to get a pull request through to master.

**Next Week’s Goals**

My goal is to get the animation system finally in place and move on to expanding the tile class.

**What I Learned**

Refactoring will be an unseen time sink in our development. This is mostly due to us using a basic engine from a previous project.

**Morale**

My morale is slightly lower than last week’s since I had to work on an assignment for another class. This coming week though, I don’t have anything due so I can get back into the groove of game development.

## Austin

**Last Week’s Goals**

Restructure the scene structure that we originally had and to refactor the project in a more sensible way, as well as working to create a prototype for the build phase of the game.

**Completed Goals**

A lot of the progress I made ended up causing some commotion within the group as we came to terms standardizing some software design patterns. However with the help of the team, the refactor has been very close to being finished.

**Unmet Goals**

Since refactoring took up a lot more time than expected, and I also had some other activities I had to deal with for this week, we ended up not being able to complete the prototype for the build phase as of yet. However it seems that our foundations for the project are a lot more stronger, and so we should be able to have it completed soon.

**Next Week’s Goals**

Finish up all the remaining functionality needed to complete the build phase prototype with the team, and then start focusing on creating the base classes and interfaces needed for having various types of game objects in the scene so that we may start moving towards the exploration phase. 

**What I Learned**

I have learned a lot this week regarding various software design patterns and conventions. I am aware that I do not have as much experience working on programming projects as my other team members, and therefore I believe I still lack a lot of intuition regarding proper software principles that are needed when designing a robust and extensive game engine like our own. These principles include things such as proper memory management and decoupling code. I believe that in the general indie game development community, there is the idea that "visual progress" is what you should aim for, however I’ve come to realize that in a software engineer’s perspective, that can easily lead to failure for big projects such as ours. Being blinded by visual progress can lead to messy code that would end up limiting your game’s capabilities, and therefore it is when we build the foundation of the game that we should try to be as organized and efficient as possible to allow for as many of the possible creative ideas we have in the future to seamlessly integrate with our game. Throughout the rest of this project, I will try to learn from this new mindset and strive for becoming a better software engineer with the help of my teammates so that I can make use of this experience in my future career as a game developer. 

**Morale**

I am always highly motivated to work on this project. I have also finished up my extracurricular team activities, and will therefore be dedicating much more time to the project than I have been.  Although I am aware that I have caused some commotions within the team, I am very glad that they have taken the time to help me learn from my mistakes. I want to continue bettering myself through this project, so I will continue to work at the best of my abilities, even if I may make mistakes. We have a lot of work ahead of us, and it’s already week 4. We’re already close to the halfway mark and have not made much visual progress, but I have a lot of faith in our team that we will be able to complete the game that we sought to achieve. 

## Joshua

**Last Week’s Goals**

Prototype of the Build Phase, by way of integrating (and finishing) UI with game logic via event/signal/message system. More specifically, raw inputs is translated into gameplay-semantic event dispatches, which UI and game logic modules subscribe to and perform work accordingly.

**Completed Goals**

The way to create UI elements and arrange them in relation to each other and the window is clear. One can readily build more specific and useful UI modules upon the system that is in place. In that sense, extensible.

**Unmet Goals**

Have not exactly integrated UI and game logic into a "Build Phase" (as described above), at time of writing. Will be worked on at time of reading.

**Next Week’s Goals**

With the basis of the game engine + networking + graphics in place, we must now look to higher-level game development and partitioning of tasks there. Concretely, a more concrete Build Phase beyond janky prototype. Look into a bug with our physics engine that, peculiarly, only occurs when we use the optimized "release" Bullet libraries. Create more UI modules (read: Textbox, Prompt, Scrollbar) for the expedience and joy of other team members (in spite of my own). Lastly, be better at making realizable goals given the lack of urgency that always fails to propel my efforts.

**What I Learned**

I relearned that age-old adage -- a mantra of my grandmother (who wants it al dente) -- that: game engine architecture is literally nails. Thus, I have been looking into game programming patterns (as have some other members of the group) with an aim to dress the wounds and patch the holes and suchlike.

As well -- pristine, decoupled, and otherwise "cool and good" systems mandate time and revision. Most notably, time. I redid my UI system from scratch one-and-a-half times over seeking that ideal.

Repurposing "tangentially related code" is tedious. Rightfully so. I learned that we should’ve started from scratch, in hindsight-tinted glasses.

**Morale**

Morale is alright,  I’d reckon.

Considering that we are somewhat behind our intentions, morale is alright notwithstanding.

Alright, back to work. (He says, with grin furnished. Donning the mask once more to hide internal turmoil. Read nothing into this.)
