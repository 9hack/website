---
date: 2017-06-15T00:53:22-07:00
title: Final Project Review Document
menu: main
weight: 5
---

## Main Questions

**Game concept: How and why did your game concept change from initial concept to what you implemented?**

We actually stayed pretty true to our initial concept. For the most part, we stuck with and managed to implement our proposed game.  However, there were several features that we chose not to implement or didn’t end up implementing for some reason: inventory, equipment, upgrades, and a combat system.  These were ideas that deal more with player progression, and are more closely tied to the "dungeon crawler" aspect of our game.

**Design: How does your final project design compare to the initial design, and what are the reasons for the differences, if any?**

The original concept art tended more towards a fantasy, grungy, dungeon-y, kind of look, whereas now we scrapped equipables (swords, armor) and went for a lighter, quirky, dream theme. The changes were really because we were unsure of the entire game’s theme and were tossing around ideas for a particular aesthetic. When looking at the concepts for characters, the animal/object type characters were more unique and fun to look at, so we decided to go with that. We wanted players to be attached to iconic characters and fight with friends who gets to be who.

The choice to include the mascot character was an excuse to have the tutorial dialogue introduced by someone. We decided to tie it in with an inside joke that started at the beginning of the quarter, and so "Sandma" was born. In the end, it actually worked out nicely with the entire theme and we decided to make Sandma Sharon have deep meaning behind her concept and inception.

**Schedule: How does your final schedule compare with your projected schedule, and what are the reasons for the differences, if any? (You should be able to glean this from your status reports.)**

We ended up getting off schedule (delayed) pretty early in the quarter — perhaps from setting too high expectations, or from a slow start in development.  We had initially reserved the last two weeks for alpha and beta testing, but we ended up using this time for development on many of our core features.  However, once we decided on our team structure halfway through the quarter, we were able to get back on schedule to some extent.

## General Questions

**What software methodology and group mechanics decisions worked out well, and which ones did not? Why?**

* **Richard**: In the initial weeks, our team had a flat structure - which felt quite disorganized since people weren’t really sure what to work on.  Once our group decided on some structure to our team (having some leaders), we had a better idea of the direction of the game, what priority to assign tasks, etc.

* **Joshua**: We used the standard git workflow wherein one works on feature branches and then submits a pull request. Thereupon, the committer assigns reviewers and (sometimes) a bounty of real money/cryptocurrency so reviewers are more motivated to review.

**Which aspects of the implementation were more difficult than you expected, and which were easier? Why?**

* **Richard**: Implementing basic networking through the Boost ASIO library and Google’s protocol buffers wasn’t as difficult as I thought, and I was able to integrate it quite easily into our project.  However, optimizing the network code and troubleshooting related bugs was quite difficult.  Particularly, Boost has really undescriptive error messages in the form of numeric error codes.

* **Joshua**: Various graphics things: e.g. instanced rendering (more information below), HDR, bloom, shadows, text rendering, turned out to be easier than I expected. There is an abundance of information on the world wide web when it comes to OpenGL techniques. On the other hand, creating a UI library at once robust and extensible, accounting for every possible thing one could ever want to draw, turned out harder than expected. Turns out: quite difficult to anticipate every scenario where one would like to inject/compose UI elements.

* **Kavin**: Scene switching had many unexpected bugs that came along with implementing it. We started scene switching pretty far into development so we had to pinpoint a lot of assumptions that we had made throughout our code that would only work with a single scene.

* **Ethan**: Ironing out the core game loop proved to be both easier and more difficult than I had expected. I wanted to allow timed callbacks throughout our code without blocking, yet keep the entire program (minus some ASIO networking stuff) single-threaded. I ended up reading up a guide on how to write a game loop without including assumptions about render and logic update time. I basically had to keep track of several time deltas, and update a variable number of times corresponding to how far the game is behind real time. As I was implementing this, I was able to implement a timed callback system as a vector of clocks that would tick down on each update. This way, any part of the system could request a timed callback and not have to worry about its execution. In one simple system, I had elegantly solved both the logic of timed callbacks (which paved the way for GUI animations and an in-game clock), as well as keep our game running at an even rate. The main difficulty came in testing, since there are real-time constraints involved in debugging. I ended up doing a lot of visual / print statement debugging, since using an actual debugger would throw off timing calculations.

**Which aspects of the project are you particularly proud of? Why?**

* **Daniel:** I am quite proud of our sound engine. It is really straightforward to use: you only need to include the audio file in the project, add the path of the audio file, and emit an audio event to play music or sound. I am also really proud of the spatial sound effects feature of our sound engine, where close-up sounds are louder and distant sounds are quieter; I came up with a mathematical model that works really well.

* **Kavin**: I am particularly proud of the minigames that our game has. We were very close to scrapping the minigame aspect of our game but Richard and I were able to get scene switching working about a week before the due date. After that, I spent the last week of development churning out 3 minigames to add to the game. It was very tedious and I didn’t sleep for almost 48 hours straight but seeing the audience’s reaction to them made the entire ordeal worth it.

* **Ethan**: I’m very proud of the event system I designed, as it permeates practically every aspect of our code. Given the event-driven nature of games, I pushed for using an event system early on to make it easier to decouple each independent system. I went in with the intention of being able to write tests for every part of our game, but as expected, these plans fell through. However, the capability is still there - in the early weeks, I wrote a test suite for one of the modules I was working on, and events allowed for flawless mocking of external dependencies. It has greatly eased the process of integrating modules together.

* **Christiane:** I’ll show my bias and say that I’m proud of the visual design of our game, it’s like my baby! I think every asset worked out to be cohesive with each other and the overarching theme really showed through. Having all the assets match made the game look polished and complete in the state it was in (even if some things were rough beneath the surface :P) I’m a little prideful, to say the least. It's always a little plus to your ego seeing your designs put to use on a big project like this. But in all seriousness, I’m proud of the entire team for bringing it all together and making my artwork shine. Without the game logic, my models would be useless! I also have to say props to the minigame dev as well for really pulling through at the last minute. It gave the game a lot of potential and really engaged the audience to root for the characters.

**What was the most difficult software problem you faced, and how did you overcome it (if you did)?**

* **Richard**: The hardest software problem I personally faced was implementing scene switching.  Since I was primarily focused on networking, I had to dive into a graphics and physics task that no one else seemed to want to do.  Doing this helped uncover a lot of bugs, but after struggling through it, I became much more knowledgeable about that side of the code.  Doing this helped lay the infrastructure for things like minigames.

* **Joshua**: More of a graphics optimization problem if anything, but the sheer number of game entities (with graphical counterparts) that we could potentially have in the scene at any given point -- especially without the use of culling optimizations -- meant a proportional drop in framerate. To solve this, we used instanced rendering to reduce the number of render calls (from being linearly proportional to a constant amount). This worked especially well for us because we had many entities that were exactly the same except for their positions in the world (e.g. the map tiles) -- prime targets for instanced rendering.

* **Christiane:** The most difficult problem I faced with Blender was setting up armatures. This was the worst thing to deal with because if you don’t assign weights properly, the model just destroys itself when it is put in the game, either by making wonky arms or clipping through itself when it should not. Some fixes to this is making sure every part of the model is assigned to a bone in the armature, or setting Location, Scale, and Rotation initial position by selecting the entire model (excluding the armature) and hitting Ctrl+A. In the end, my models still broke in one of the minigame phases of our game and I cry every day since the demo

**If you used an implementation language other than C++, describe the environments, libraries, and tools you used to support development in that language. What issues did you run into when developing in that language? Would you recommend groups use the language in the future? If so, how would you recommend groups best proceed to make it as straightforward as possible to use the language? And what should groups avoid?**

* We did not use any languages besides C++.

**How many lines of code did you write for your project? (Do not include code you did not write, such as library source.) Use any convenient mechanism for counting, but state how you counted.**

* **18,243** lines.  To find this, we executed this shell command in our project’s source directory, making sure to exclude any library files and auto-generated files.

`find . ! -name 'catch.h' ! -name '*.pb.*' -name '*.*' | xargs wc -l`

**In developing the media content for your project, you relied upon a number of tools ranging from the DirectX/OpenGL libraries to modeling software. And you likely did some troubleshooting to make it all work. So that students next year can benefit from what you learned, please detail your tool chain for modeling, exporting, and loading meshes, textures, and animations. Be specific about the tools and versions, any non-obvious steps you had to take to make it work (e.g., exporting from the tool in a specific manner), and any features or operations you specifically had to avoid — in other words, imagine that you were tutoring someone on how to use the toolchain you used to make it all work. Also, for the tools you did use, what is your opinion of them? Would you use them again, or look elsewhere?**

* **Kavin**: I highly recommend that future groups get their importer working for models/textures/animations/etc very early on in the quarter. We used Assimp as our import library and Blender as our modeling software and throughout the quarter we had to go back to our asset importer to make adjustments. If we didn’t get our importer working as early as we did, we would have had a much harder time making good assets for our game. I would use both Blender and Assimp again, I just would be more careful with using Blender; Blender works well with importing and is user-friendly when it comes to creating models but there is a very specific method in which to work in order for your assets to properly get loaded into the game. To the artists of future groups: check your armatures well or your model will explode in game. 

* **Christiane**: Seriously, check the armature and weights of your models in Blender before you import it. If you don't know how to do something, at the very least youtube has a plethora of helpful tutorials to get you started. Other info can be found in forums. You can use Open3Mod for a little taste of how your models appear when you import them into the game and to check if your animations work. But sometimes Blender will play tricks on you and it’ll look good in both Open3Mod and Blender but when you import your models, it’ll break and you will cry. Just try it out early on for troubleshooting with the engine. Aside from this, because animating models in Blender requires assigning weights to bones of the model’s armature, if your model is all one object sometimes it squashes your model when trying to move an arm or something. A workaround I did, since we decided on low-poly models, was to have separate objects for the the arms and legs and for the body. That way you can animate it independently without stretching or skewing the rest of the form. However for more organic, realistic models, this is fine. Be sure any extraneous objects you add to your model is properly weighted or when your character moves a certain way it'll leave something like its ears trailing after it. Also, have a base model because it makes things easier to animate and all you have to do is a bit of cosmetic changes to make different characters. You will thank yourself later by having a base because you don't have to figure out all the rigging for each individual model and focus on the animation itself. Save a lot of copies of a file and be sparing with your overwriting. Aside from this, also be attentive of your model colors in Blender. If you choose to texture it, this may not apply, but if you color your models by "hard coding" it (aka assigning colors to each face) what you see in the Blender screen will appear darker in-game. You can preview what the colors looks like in Open3Mod. If you choose to use HDR in your game, then what you see in Blender is what you get. 

**Would you have rather started with a game engine or would you still prefer to work from scratch?**

* **Richard**: It would have been nice to be able to work with Unity, as this would require a fraction of our development time.  However, I think this would void the purpose of the class, and not make it as challenging.  There’s a certain pride we get from writing everything from scratch - the UI library comes to mind.

* **Joshua**: Certainly starting with a game engine would have given us substantial license to create, in terms of gameplay. In fact, the majority of our gameplay was implemented in a disproportionately tiny sliver of time, compared to the engine and the bugs that came with. With a third party game engine, most of what we worked on would have came for free and bug-less (for the most part). This being said, Richard is right in saying that it would essentially void the purpose of the class. Granted, we could have probably implemented the same game in a fourth of the time if we started with a game engine -- that’s literally no fun at all though is it?

* **Ethan**: I feel like working with an existing engine like Unity would be nice, but the cost of learning it and trying to implement our game’s logic on top if its framework might have been difficult. In particular, features like modal input and separate gameplay phases may not have worked out as easily. The "Unity" way of doing things might restrict our ability to implement our vision.

* **Christiane:** I know *technically* I didn't work with the engine development so I can’t comment on this. But I have to say that working from scratch, at least for making models, is the way to go. It’s your pride and joy to make your own assets! You have the freedom to manipulate it into anything you want and you can let your creativity shine through. Yes, it's a pain for all the steps required to model, rig, animate, troubleshoot, etc, but it's so worth having your *own* work. I’m kind of a stickler for using artwork that isn't yours for anything more than a placeholder, so it's vital to have original art so you are not relying on someone else’s pre-existing work. Plus, it's no fun if someone is using the same premade models in their game and now you both have identical assets!

**For those who used a networking library (e.g., RakNet or Boost), a physics library (e.g., Bullet), or a GUI library, would you use it again if you were starting over knowing what you know now? Describe any lessons you learned using it (problems that you had to troubleshoot and how you addressed them) for future groups who may use it. If you did not use a library, judging from the experiences of the groups that did, would you have used it in retrospect?**

* **Richard**: We used the Boost ASIO networking library.  If we were starting over, I believe I would still use it again - it was fairly easy to integrate into our existing codebase, and cross-platform (for our one Mac-developer).  However, the documentation on it quite lacking.  And whenever I encountered bugs, the error messages are quite unhelpful, which involved a lot of Googling and looking at example code snippets.

* **Kavin**: I would definitely use Bullet again. It allowed us to focus on other aspects of the  game engine but still reap the benefits of extensive collision detection and physics capabilities. I would recommend implementing it early on though so that your code can integrate it properly. Once the framework for it is set in stone, Bullet can be a very powerful ally for CSE 125.

**What lessons about group dynamics did you learn about working in such a large group over an extended period of time on a challenging project?**

* **Daniel:** Everyone has different schedules and responsibilities, we just have to be flexible and work around them and remind each other about the current status of the project and whether something needs to be done.

* **Kavin**: There’s the saying of never do business with family or friends but I feel as if us being friends is what allowed us to work so well together. Our entire group was already decided before we joined the class since we all knew each other one way or another. If you had to stay up throughout the night together and be constantly frustrated over broken code, being good friends is what keeps you from being at each other's’ throats.

* **Ethan**: As a flip side of what Kavin said, if you do have a problem with someone’s code, it might be more difficult to express that. Our rigorous code review process was what allowed me to still express these opinions, with no risk of hurt feelings.

* **Christiane:** Even though technology allows us to communicate with each other easily, it is still best to work all together in person. It's difficult to articulate a problem over messenger without 1) showing the problem in action and 2) explaining in full detail in a concise way without the other person missing critical information. That's why it's best to get your schedules aligned so you can really optimize your time together. Tasks get done a lot faster, and you can ask for help if there's too much to do. Also even though we didn't have a "project manager" role, the false sense of security of making someone take “leadership" helped get tasks dealt with instead of no sense of direction.

**Looking back over the past 10 weeks, how would you do things differently, and what would you do again in the same situation?**

* **Richard**: Looking back, we should have decided on a team structure early on, which would help guide development and game direction.  On the other hand, I would have taken the leap of faith to work on minigames again - it was a big gamble at the time, but we managed to complete and and complete it well.  Having a system for code reviews also ensured our code was of decent quality.

* **Joshua**: Already a fourth of the way into the quarter, we made some hindsight observations -- we should have not started with a skeletal engine that originated from CSE 167, which was meant for a graphics demo and not a game demo. Instead we would probably be better off starting from scratch and perhaps consulting the skeletal engine occasionally for reference (not for copy). Also, we maybe should have worked more/earlier in the labs. The last two days (and nights) were probably our most productive, because we eliminated the temptation of sleep by forcibly imprisoning ourselves, fermenting overnight in the underground chambers. Regardless, our outcome was unanimously good, so maybe the relative comfort of non-lab venues proved beneficial -- one will never know.

* **Christiane**: Adamantly push for a theme. I felt like I couldn't just decide on an art style since everyone was very neutral to having it one way or another and I was hung up on what to base the design on without a central theme. Also there were ways to make modeling characters off the concept art a little easier by importing the reference image into Blender, but I decided to just freehand it. The indecision lead to redoing models often because I was unsatisfied.

**Which courses at UCSD do you think best prepared you for CSE 125?**

* **Daniel**: MUS 173 prepared me for music and sound effects design. I learned how to use Ableton in that class it is very useful when it comes to producing soundtracks or making and editing sound effects. CSE 124 definitely prepared us a lot for the network aspects of our game. We learned how to design good and reliable network protocols.

* **Joshua**: CSE 167 is an obvious one. Game engine development demands a familiarity with 3D rendering libraries and real-time rendering techniques. As it’s a full-on course in itself, doing without it is tantamount to doing without a prerequisite.

* **Richard**: CSE 124 for networking.  We learned a lot about socket-level programming, which helped us establish the server-client setup.  Also, having exposure to RPC’s through Apache Thrift made it easy to integrate protocol buffers.

* **Ethan**: This is kind of cheating, but CSE 197. Doing internships helped me learn about networking more than any class here. Having real-world experience with protocol buffers made it an obvious choice to use for shuttling data between client and server, and I was able to share the best practices I had picked up.

* **Christiane**: This is cheating too because all my art making experience is self-taught. So really this is my two cents on "PRACTICE PRACTICE PRACTICE" if you want to get good at a skill in real world applications, like Ethan said.

**What were the most valuable things that you learned in the class?**

* **Daniel:** We learned how to work with a big team on a big project.

* **Richard**: I learned a lot about architecting the game, and server-client abstraction.  This was also a great chance for me to apply software design patterns I had learned in class (in addition to new ones) and apply them to an actual project.

* **Kavin**: Game design and architecture. Nothing really teaches you about designing a game engine like creating a game from the bare basics.

* **Ethan**: I learned how to quickly pick up someone else’s code and run with it. Since I’m kind of a jack of all trades, master of none, I ended up lending a hand to a lot of different parts of our code. It was a struggle understanding what was going on at first, but I got better at reading intentions behind the code over time.

* **Christiane**: I think the course itself is the most valuable. I've never had a course that had such a direct, practical application to the work environment I hope to be in. Learning how to work in a specialized team for an entire quarter is something that is so vital for working successfully with others in a company after graduation. I was able to get a feel for the workflow of making the initial 2D artwork, then learning 3D modeling (super important), and seeing it put into the end product. There is something so satisfying seeing your art turn into something fun and tangible.

**Please post four final screenshots of your game on your group pages for posterity. I will display them on the group web page.**

* COMING SOON!

## Course Feedback

**What books did you find helpful that were not on the recommended list but should be? What books were on the recommended list but were not useful and should be removed?**

* **Daniel**: Not a book, but I definitely recommend future students to check out the SFML Library. Even though I only used the audio library, they seem to have other libraries for graphics. The audio library was reliable and relatively straightforward to use.

* **Austin**: *Game Programming Patterns* by Robert Nystrom helped me a lot in learning some fundamental software design patterns that we implemented in our system architecture. This should definitely be on the recommended list for the following years, as it goes through many situations that we faced when designing our engine. The book is also free to read online: http://gameprogrammingpatterns.com/contents.html

**I will be teaching this course next Spring. What advice/tips/suggestions would you give students who will take the course next year?**

* **Austin**: Our biggest issue was that the graphics and networking teams were working separately in the beginning, making it difficult to integrate our code together. I would definitely recommend that the graphics and networking teams have at least one person constantly communicating and integrating their systems together, to make sure that time is not wasted later on changing code to fit the other’s system.

* **Richard**: Definitely take advantage of all the resources available.  For example, I think a lot of teams can benefit from integrating game controller input (though this is just my opinion).  Besides that, just make sure to be extra communicative, and have a mandatory process of code review to ensure quality and that everyone’s aware of what’s going on.

* **Kavin**: Be very careful with how you implement your base game engine. A fleshed out, flexible game engine is what allows you to go far with your game ideas.

* **Ethan**: From the very beginning, force a code split between client and server. Taking the hard way out at the start means you don’t have to refactor later on.

* **Christiane:** Google is your friend

**How can the course be improved for next year?**

* **Austin**: I feel that all teams should have at least one designated artist. Having a good-looking game definitely affects a team’s morale. Also, have class be later in the afternoon… (I am not a morning person)

* **Ethan**: To add to Austin’s point, each team should have someone that is somewhat proficient in sound. During the demos, we really noticed some games where sound design was not a priority, and it really hampered the subjective quality of the game.

* **Daniel**: Adding to Ethan’s point, we originally placed sound as a nice-to-have goal, but then we started realizing its importance halfway through the quarter. Though I have never composed a soundtrack or worked with sound effects before, I have enough music background to do both the sound engine and the soundtrack/sound effects.

* **Christiane**: It should be reiterated to make it fun! I think some people might get hung up on super nice graphics or functionality, but forget that it's a game, and ultimately you want to enjoy playing it. That isn't to say those two things aren't important, but a game can still benefit having less "functionality" or extreme high rendered backgrounds if the overall base mechanics are fun. Make a game you wouldn't mind buying because it's fun.

**Any other comments or feedback?**

* **Austin**: Thank you for this wonderful opportunity. There were a lot of struggles going through the quarter, but amazing the entire audience during our final presentation definitely made everything worth it. This was an unforgettable experience, and has made me more determined to pursue my passions in game development.

* **Daniel**: With the number of people working on this project, I didn’t expect the high commitment and workload. But I am glad that it all worked out well in the end. It was a great learning experience and taught me how to work with people from different backgrounds (e.g. graphics) and how to produce one cohesive final product.

* **Christiane:** Working on an extensive project like this was the best experience in all four years of my undergrad career. It directly correlated with my dream job, since I want to become a video game concept artist since, I don’t know, 2007? 2008? I was getting concerned because here I was with this lofty goal and no game development experience to back it up. I honestly had no idea this class existed until Ethan mentioned it during Week 1 and I was extremely excited to work. Thank you for offering such a unique, hands-on course like this. It really reinvigorated me, like Austin mentioned, to see all our hard work come to fruition and get such an awesome response from the audience when they saw what we had created together. I admit I still had the recurring doubts about my career choice halfway through the quarter, such as "are artists really in demand in this industry?" or “maybe people won't like the art direction I chose.” But seeing that someone even went so far as to compliment our game’s art style during the final demo was so touching that I knew that a game’s visuals are just as important as the mechanics. Now I can go forward confidently and aim to make more art that people will definitely love in their games.
