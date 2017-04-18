---
date: 2017-04-17T20:53:33-07:00
title: Week 1
---

## Group

**Weekly Status**

We decided on a visual theme for the game, and developed initial concept art for how characters and in-game objects look.  We also drafted a mockup of how the game should look when played.

This week, both the graphics team and the networking team worked on setting up our respective basic functionality.  For the graphics team, the following features are now implemented:

* Able to load ASSIMP FBX

* Bullet physics engine integration

* Mouse picking using raycasting

* Text rendering

* Basic rendering pipeline

* Shadows

* Event system

For the networking team, we have research networking libraries and decided to use Boost ASIO - not only for cross-OS compatibility but for its general purpose capability.  We have used this to implement sending messages between a server and clients, and will continue to develop upon this in the following week.

**Meeting Date**

Week 2: Saturday, April 15

**Group Morale**

Our collective morale seems to be leaning slightly positive, with about half feeling enthusiastic but the other half disappointed (or sick).  As this is the first week of development, we hope the excitement will carry forward to future weeks, but understandably this stage is the most tedious due to the amount of setup and configuration needed.  If we had more tangible or visual progress, we reckon morale would be higher as well.

**Screenshots**

![Week 1](/img/screenshots/week1.png)

Additionally, we also have uploaded some concept art
[here]({{< ref "pages/concept-art.md" >}}).

## Ethan

**Last Week’s Goals**

My goals were to get our team website up and running, investigate networking libraries, assist in developing an event system, investigate unit testing options, and get our existing codebase working on my computer (which is the only Mac in our group). I also started to investigate options for gathering joypad input.

**Completed Goals**

I was able to easily get our team website up using Hugo, a static site generator that had caught my eye for some time. It allows us to quickly author new content to our pages in the easy-to-write Markdown format. I encountered a little bit of difficulty replicating the setup on other members’ computers (in particular, permissions weren’t being re-set on re-deploy), but it wasn’t too much trouble.

I looked into GRPC (Google’s RPC library) and Boost ASIO a little bit, but as Richard got more headway on this, I left the remainder of investigation to him.

After a few iterations, I finalized the event system that our team would be using with the help of Joshua. It took a few tries to nail down which parts of the system we wanted to make generic, but we ended up with a concise implementation in under 20 lines of code.

After a long night of struggle, I also successfully got our existing graphics code to compile on my Mac. It involved some weird Mac-specific things, like "downgrading" the OpenGL version just for Macs in order to use the correct version.

**Unmet Goals**

Unfortunately, I was unable to secure a good unit testing solution for our group. It turns out that while setting up unit testing using a Makefile or CMake is trivial, doing the same with Visual Studio is not. Since everyone except me uses Visual Studio, this is obviously a major factor. I did my best to work with another member to see if any solutions I had found would work on their setup, but did not make much headway. Unfortunately, I cannot make make much progress by myself on this front because of my OS restriction. I plan on either assigning this task to another member which does have Visual Studio, or reprioritizing it for later.

**Next Week’s Goals**

My goal for next week is to have fully a functioning joypad input abstraction layer ready to deploy in our primary codebase. I also plan on assisting Richard with working on our networking stack, and will likely set more milestones for myself as we understand more about the library. Finally, I hope to get a good VS-compatible unit testing framework in place.

**What I Learned**

It was unexpected, but I learned that even big ideas can be distilled into few lines of code if done correctly. Originally, I had thought that our event framework would involve threads, an asynchronous event loop, event queues, and a lot of other machinery. However, as I went through prototyping iterations with Joshua, we found that an almost painfully simple solution could do as much heavy lifting. We finally settled on an extremely simple single-threaded header-only "library" which still fit our needs.

**Morale**

I have 4/10 morale, if only because of all the difficulty I’ve encountered in getting my development environment to parity with Visual Studio users. Not many members are accommodating of my hardware limitations, suggesting we use Windows-only libraries everywhere… I find it hard to feel like I have a place in the project sometimes. I’m quite satisfied with our game concept though, so I’m not entirely disillusioned.

## Richard

**Last Week’s Goals**

My goal for this week was to go through the Boost ASIO tutorial to gain an understanding of the networking library, and to evaluate it.  If it turned out to be unfit for our needs, we would look at other libraries.  My goal was also to set up a basic network client and server interaction (sending data between each other).  Another goal was to lay out a basic protocol design.

**Completed Goals**

I was able to go through the ASIO tutorial and use it to write an asynchronous server and client that can read and write plaintext messages to each other, running in 300 ms and 100 ms loops respectively.  I was also able to integrate this into our Visual Studio project and have it run successfully, albeit with no remote server connected.

**Unmet Goals**

I was unable to do much server functionality besides sending data, such as message partitioning and protocol implementation.  This is because, as I later realized, that Boost ASIO has a bit of a learning curve, so it took me some time to get used to programming with it.  Additionally, getting the library linked correctly on Windows was more time consuming than expected.

**Next Week’s Goals**

My goal for next week is to continue my integration of the network code into our Visual Studio project.  This involves adding message partitioning, and making the client perform some action based on a server message.  Also, a goal is to prototype a basic protocol that can be used as the message format for communication.  If time permits, I plan to test extensively (as this is a key part of the game) on multiple machines.

**What I Learned**

I learned a lot about asynchronous network programming - I had some experience with it before, but learning about how Boost’s ASIO library utilizes it was an eye-opening experience.  Unexpectedly, I learned a lot about Visual Studio projects, specifically setting up dependencies/libraries and linking.  This was my first time working on an actual project on Windows after doing most of my development on Linux, so I had a lot to learn.  Needless to say, I learned that developing on (or for) Windows is painful. :(

**Morale**

I rate my morale at a 6/10, mostly because of getting stomach flu midway through last week and having to code despite that.  Also, getting things set up in Visual Studio and Windows was more complicated than I expected, which contributed to this score.  However, I was able to achieve most of my goals, which is a big plus.

## Daniel

**Last Week’s Goals**

* Get a game idea down

* Research on libraries to do TCP

* Website

* Produce some art assets

**Completed Goals**

I was able to join in the discussions for the game idea; I wrote down the specifications for our first meeting. I did some research and tutorial on the C++ Asio library. I produced concept art drawings for our game map.

**Unmet Goals**

I wasn’t able to do more research into other libraries to make the server connection. Our team hasn’t decided on what to use yet.

**Next Week’s Goals**

* Decide on a library to use to set up the server connection

* Assist with art assets

**What I Learned**

I learned how to update and deploy the website that Ethan set up using the Hugo framework. C++ Asio library feels painful. We are currently debating whether to switch over to Python.

**Morale**

I am glad we have a game idea that everyone seems to be ok with. I look forward to the stage of development once we have the frameworks set up, which is always the boring and painful part for me. I am excited to see the art design of our game and see what ideas I can come up with for the music.

## Christiane

**Last Week’s Goals**

This week’s main objective was to develop initial concept art sketches and determine the overall theme of the game with the entire group. Since there wasn't a set concept for art design, I came up with a beginning idea to present to the rest of the group so we could work together on a game style to move forward with.

Other additional goals afterwards was to think up asset designs and begin working on implementing designs into 3D models.

**Completed Goals**

I was able to create character designs that will fill the roster for players to choose from. Some stage designs were also made for the group to decide on a theme and gain a more solid understanding of what the team envisions for the final design.**Unmet Goals**

I was unable to do start testing on 3D modeling because I went out of town but my keyboard stopped working so I was unable to log into my computer. However I was able to get a gist of the initial steps and once I get a chance to, will actually try out the process on the program itself.

Technical difficulties occur and I need to have a contingency plan and backup computers to keep doing work, but in this scenario I just have to wait to get home to continue work.**Next Week’s Goals**

Next week’s plans are going to include refined character design and more level design, as well as starting to model assets to give to the team to implement into the game.

**What I Learned**

I found out that it is difficult to design as a whole without much of a thematic direction. However, I know it is part of the collaboration with others that requires me to put an idea out and have things stem out from there.

I also learned how even from initial concept creation we have to keep in mind the graphical capabilities (such design and object complexity) since putting excessive details into a design is not as feasible.

**Morale**

My morale is currently very enthusiastic for the most part. I am a little worried at the scale of the project as well as how some tasks are going to be outside my comfort zone but I am excited to learn new things. My career goal is actually to become a video game concept artist, so this sort of experience is very valuable to me.

## Kavin

**Last Week’s Goals**

I wanted to get a basic grid system in place to support the build phase of the game.

**Completed Goals**

I was able to set up a grid system using tiles that inherited from a superclass Tile. Hopefully by using polymorphism for the tile classes we can implement more tiles in a quicker, more streamlined way. I was also able to incorporate Bullet Physics into our project and use their collision detection and raycasting to implement mouse interaction with the grid. As of now, the click callback doesn’t do anything but the functionality to allow for clicking on the tiles is set up. Also basic fbx model loading with Assimp is in place.

**Unmet Goals**

So far there wasn’t any goal is was not able to meet but this is probably due to its being just initial code setup and structure creation. Once we get into the nitty gritty of implementing the individual items/tiles, goals will be more aggressive since the scope of implementation will be much wider.

**Next Week’s Goals**

Get full fbx loading (meaning model, material, texture, and animation). Start to implement functionality to change out tiles in the grid and add more tile classes.

**What I Learned**

I learned about the basic workflow of Bullet Physics and Assimp. I was expecting to learn it since these libraries were decided to be used early on in our group.

**Morale**

I am eager to continue working on the project. I still have some trepidation with whether or not we will implement our entire project but I believe in my team’s abilities to push for the finish line.

## Austin

**Last Week’s Goals**

My initial goal for the week was to focus on the loading of various assets using the *assimp* library, however towards the end of the week I focused more on cleaning up the current scene graph setup that we had. 

**Completed Goals**

I figured out basic integration of assimp into our project, and cleaned up the scene graph by removing functionality that was used in a previous project that would no longer be used.

**Unmet Goals**

I ran into a lot of difficulty with time management this week, and therefore did not make as much progress with the asset loader as I had hoped.

**Next Week’s Goals**

I will be assisting with the integration of the asset loader into our system, as well as create an intuitive structure for organizing the models that are to be rendered in a scene. I will also aid in any of the other systems that may be required in having the build phase for our game working properly. 

**What I Learned**

I learned a lot about event-driven architecture as I worked alongside my teammates who were implementing it. 

**Morale**

I am disappointed in myself for not achieving as much as I wanted to last week, and will therefore push myself in order to work with my team and have a functional prototype of one of our core systems by the end of the week.

## Joshua

**Last Week’s Goals**

Text and UI rendering, and an event system for our event-based architecture.

**Completed Goals**

I was able to get basic text rendering in OpenGL done, along with some design options for the event-based architecture that our game will employ. UI rendering is thus far unfinished, but a pretty clear idea is in the mind.

**Unmet Goals**

I was unable to implement a UI rendering system; I was going to do it today, but some health stuff obstructed my progress. I will probably do work on it after this writing this report.

**Next Week’s Goals**

Do basic Build Phase of the game via merging UI rendering with the grid system/higher level game logic that Kavin has implemented, whilst integrating input to link the two.

**What I Learned**

Learned how to do text rendering in OpenGL, which involves using the FreeType library to render TTF fonts onto bitmaps, then rendering the appropriate texture onto quads.

**Morale**

My morale is tempered, that is weighted, by my energy level. And considering my illness this past week, both have been relatively low. I will hereinafter pick up the pace, not only because of recovery but because of time pressures closing in (that is, the milestones/schedule we set in the project specifications).

