---
date: 2017-05-08T20:53:33-07:00
title: Week 4
---

## Group

**Weekly Status**

* Server timer + timed game loop

* Server-controlled player movement, ability to see other players moving around

* Phase change broadcasts from server

* Added ability to place multiple lights in the scene: directional, point, and spotlights.

* Collision detection in place, as well as trigger objects.

* Proper camera controls using game joysticks for build and dungeon phase

* Dungeon generation using a text file

**Meeting Date**

Week 5: Saturday, May 6

**Group Morale**

Fairly positive overall. The group is generally happy with the progress we have made this week and are all working hard as we pass the halfway point of the quarter.   We’ve reached a point where the game’s core engine and infrastructure is nearing completion, and it’s time to polish our work and further implement game logic.

**Screenshots**

![camera_test](/img/screenshots/camera_test.gif)

#### Camera
<br>

<video width="640" autoplay controls loop>
  <source src="/videos/lights.webm" type="video/webm">
</video>

#### Lights
<br>

<iframe width="640" height="360" src="https://www.youtube.com/embed/p3ol68cfX6Q?rel=0" frameborder="0" allowfullscreen></iframe>

#### Multiplayer movement
<br>

## Ethan

**Last Week’s Goals**

Finish semantic input translation API, help Daniel get sound integrated, prototyping if time permits.

**Completed Goals**

I was able to get a my input API merged in, and to my delight, others were able to transition to it very smoothly. I also was able to implement the core server timer, which also handles timed and repeating callbacks. Daniel is also making progress towards implementing sound. We were still having some compilation issues, but it seems that they have been more or less resolved.

**Unmet Goals**

I was admittedly a bit reserved in my goals last week, but having been able to meet it is encouraging. I haven’t actively prototyped anything because we partially switched to a new group organization style (reporting to and getting tasks from a centralized manager). Instead, I’ve worked on what from a high-level perspective would best benefit the team within my abilities. Since Daniel seems to have resolved most of his technical issues, I’ve been helping him design the sound API in a way that matches our current codebase style (using events, etc.).

**Next Week’s Goals**

We ran into an odd timing issue this week where the networking stack was taking ~24ms on some game loop iterations, which is odd. Since our game loop should be locked to 30ms, this is a high priority issue to investigate. As the implementer of the game loop timer, I’ve been assigned the task of pinpointing our bottleneck and improving core loop performance. I also would like to take a look at a design pattern Joshua sent me: [http://gameprogrammingpatterns.com/game-loop.html#play-catch-up](http://gameprogrammingpatterns.com/game-loop.html#play-catch-up)

**What I Learned**

On the technical side, I learned how to work with C++ timers to implement a single-threaded timed event loop. It’s by no means ultra high performance, but knowing that I’m able to achieve functionality similar to node.js with my own code from scratch is satisfying. I also found that my hypothesis from last week was correct: now that we have a more centralized leadership, it’s been easier for me to see what direction the game is going in. I’ve been able to trust that the other team members are working on the right components, so I can focus on doing what I’m good at.

**Morale**

Bumped up to 7.5/10. I’m much more comfortable with group organization now, and I’ve made solid progress on important parts of the game. I still have little knowledge of the graphics side of things, which leads to a bit of apprehension regarding the capabilities of our game. It also seems that we haven’t made all that much tangible progress towards firm client/server separation. We do have an outstanding pull request (that I haven’t been able to get around to reviewing yet) though. The quarter is over halfway over, so things are coming down to the wire… but I feel okay about where things are at.

## Richard

**Last Week’s Goals**

My goals last week were to get networked player movement integrated.

**Completed Goals**

I accomplished my goal of getting multiplayer movement working!  Currently movement data is sent from the client to the server, which updates the physics, and then sends back the calculated positions and orientations of all the players.  I also made the current phase controlled by the server, broadcasted to the clients.

**Unmet Goals**

Though I got multiplayer movement working, I realized that collision and object interaction handlers would also need to be handled on server side as well — currently it’s only client side.  However, this is dependent on a slight change with game objects (each one needs a unique ID, synchronized between server and client).

**Next Week’s Goals**

For next week, I plan to work on the above networked collision and interaction.  I imagine this won’t take too long once the game object refactor is complete, so I plan to also work on game logic.  Specifically, further developing phase changes & progression with a game timer, working on a starting waiting lobby, and any related network features.

**What I Learned**

I learned that having frequent team status updates on Slack helps us all keep tabs on what everyone’s working on, more or less.  This can definitely be done more effectively, but I’m glad that we’re heading in the right direction.

**Morale**

Morale is decently strong at a 7/10.  I managed to complete my goals, but having a pull request that my other pull request depends on go unreviewed for a while hinders my progress somewhat.  I can continue developing new features, but I don’t feel as productive knowing that the assumptions I make in my previous pull request may be incorrect.  Other than that, I’m happy with how our game is turning out visually, and game controls are quite fluid and responsive.

## Daniel

**Last Week’s Goals**

Last week’s goal was to try to set up an audio manager in our game system by utilizing the SFML library to play wav files.

**Completed Goals**

I read through a tutorial on the Boost Signal library that Ethan sent me. We decided that Signal will work well because our sounds will mostly be event driven.

I did not get our code to compile on my Linux machine. I switched to my Windows machine and after a lot of setup, was able to get it to work with Visual Studios.

**Unmet Goals**

I was unable to start implementing our audio manager because I was unable to compile our code.

**Next Week’s Goals**

I want to implement the audio manager and test it. I also plan to see how I can help with the game logic group. I will start brainstorming for our game’s soundtrack.

**What I Learned**

I learned how to set up a project in Visual Studios. I also learned how to use the Boost Signals library.

**Morale**

Morale this week was pretty low for me. I got pretty stumped when I am trying to set up our project on my computer. My Linux distribution (on my Chromebook) actually died when I am installing libraries and drivers for our code, forcing me to redownload the distro. Setting up on Windows VS is not exactly a cake walk either despite having all the config files working for other team members using VS. Luckily, Richard helped me a lot with setting up. But now I’m unblocked, I feel a little bit more positive.

## Christiane

**Last Week’s Goals**

Keep modeling assets for the game. Design levels to implement. Work on integrating assets into cohesive theme.

**Completed Goals**

Discussed some game mechanics in order to get a better understanding of what sort of assets feasible to implement in game. Created more assets with animations, edited existing assets to fix errors and add more details (i.e. fixing broken meshes on assets; adding gold to treasure chest).

**Unmet Goals**

Only created high priority and some medium priority assets, but some medium priority assets are still unfinished.

**Next Week’s Goals**Finish up existing assets that need to be created. Brainstorm up ideas for game logo/mascot to help pull game theme together

**What I Learned**

The animations currently attached to existing models are unsupported by current animation library and must be animated using bone armature in Blender. Must redo all the animations to use bones instead. I also learned how to model moving waves in Blender, but not sure how that can be implemented into game due to the fact it needs bone animation. Adding in water to game is TBD.

**Morale**

Normal to high- it’s fun seeing how the assets are being put into the game and it is exciting to watch how the game is developing into an actual game.

## Kavin

**Last Week’s Goals**

I wanted to flesh out player movement and be able to push a completed player movement module to master

**Completed Goals**

I was able to integrate joystick movement into player movement as well as organize movement and interaction with events. I also worked with Richard to split up some logic in the scene/grid/gameobject classes in order to separate out graphics related code. 

**Unmet Goals**

The only major thing I had planned was to finalize player movement so that others can start implementing new features with it. So I suppose there wasn’t any unmet goals due to the scope of last week’s goals.

**Next Week’s Goals**

I would like to start working on more constructs/traps for the game. Either that or start on the framework for minigames. The goal will most likely be determined in the next team meeting.

**What I Learned**

I didn’t learn much this week, a lot of work consisted of polishing and refactoring code and functionality.

**Morale**

Still high, though I feel as though the initial development adrenaline is gone.

## Austin

**Last Week’s Goals**

Write out some design docs and discuss with the team the remaining roadmap for the game. 

Start working on the minigame phase.

**Completed Goals**

Got camera movement working properly for both the build phase and dungeon phase. Designed a dungeon map to use for the game, and made a simple way to import a map via a text file. Made some fixes to animation to make different game objects have their own animation. Also made a short design document that gives a roadmap to the features that would need to be implemented for the final game.

**Unmet Goals**

We still require a lot more work on the dungeon phases before we can start working on the minigame phase. 

**Next Week’s Goals**

Finish up the dungeon phase and make sure to flesh it out before we can move on to the minigame phase. Specifically, work on the implementation of traps, player parameters, and more efficient rendering

**What I Learned**

Designing a game to work with networking is difficult and requires constant communication. I’m glad we got much more consistent communication within the team. I’ve also learned how spending every day and night on this project is not the best idea, and could end up causing me to do less work due to stress in the end. (Also, I’ve learned how much of a pain compiling is.)

**Morale**

100%. Starting to get more and more serious about the project as we start passing the halfway point. 

## Joshua

**Last Week’s Goals**

Get the exploration phase up and running. I wanted to see the ability for a player to move a model around in the map, with the camera centered upon the model – and be able to see other players doing the same thing too.

**Completed Goals**

The exploration phase is almost nearly definitely up and running. Richard and Kavin got the multiplayer aspect working -- being able to see other players move around. We have the camera tracking in place and player movement in place. As for what I completed, I fixed shadows (again) and added Color and Light classes to more easily manage graphical constructs. I also put collision detection in place, and trigger objects (collision callback is made but no rigidbody physics).

**Unmet Goals**

Nothing was unmet, really. Except I didn’t work on my goals as much as I wanted to -- other people completed my goals for me.

**Next Week’s Goals**

Fix performance issues when rendering many tiles via instanced rendering. Also may want to work on collision masks for powerful control over which objects can collide with each other. As well as integrate the Bullet debug drawer.

**What I Learned**

I learned about.. what did I learn about..? I learned about how Bullet does collision detection (rather, how we can set up Bullet to do collision detection in various ways). I also learned that I require more motivation to get anything done.

**Morale**

Morale is fairly high, simply put. 7/10, simply put.
