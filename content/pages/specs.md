---
date: 2017-04-09T00:53:22-07:00
title: Specifications
menu: main
weight: 3
---

**Project Description**

*Overview:*

We want to create a game that contains both the sense of exploration and discovery of dungeon crawlers, and the chaotic and competitive interactions of a party game. To combine these two together, we have decided to build a game in which players can compete with each other in mini games, use the points obtained thereof to collectively build a dungeon full of both hazards and treasures, and then traverse this dungeon while avoiding their opponent’s obstacles. Players compete to have the most amount of gold by the end of the game by avoiding obstacles, winning in mini games, and stealing from your opponents.

*General Game Flow:*

To better describe the game, we must first explain the general flow of the game. Each round consists of three main phases, starting with the build phase:

![Game Flow](/img/diagrams/phases.png)

*Beginning Phase:*

Players begin the game by choosing a character to represent them. The characters serve purely aesthetic purposes and add no special bonuses for the player other than to serve as distinguishing identifiers. Then the players must choose the parameters for the game, such as number of rounds that they will play for, and dungeon map. Once the setup is completed, the players are put into the game and are given an initial amount of gold to begin their first build phase.

*Build Phase:*

During the build phase, players are able to place various objects in the dungeon. Players will place objects on the dungeon grid at the same time, but players will only be able to see the items that they place themselves, while their opponents’ objects will be hidden.

Using the gold they have, players can buy traps or creatures and place them in locations in the dungeon that their opponents might go to in order to inhibit them or hurt them and make them drop their gold. Players may also purchase structures that can benefit them in hard to reach locations, such as a chest for getting items. However, players would need to be careful to not be hurt by their own traps, or not to lose the chests they place to enemies that get there first. The idea is that players simultaneously manipulate the dungeon for their own benefits while trying to obstruct others.

Some players may want to hold on to their gold so that they can stay ahead of others, since the end goal of the game would be to have the most gold. But this allows players who may be behind to get a head start by targeting the opponents who may be ahead.

*Dungeon Phase:*

Starting from the same initial room, players will traverse through a dungeon and race to the end portal before time runs out. The order in which the players reach the end portal decides the bonus multipliers they will get for the next minigame phase. However, players may also want to explore the dungeon in order to find chests that they or others may have placed, or to make use of any structures that they may have hidden. There may even be chests that no one knows about, that were in the dungeon to begin with. While exploring, the players must try to avoid the obstacles other players may have placed. When hurt, the player loses some of their gold and gets stunned! The number of possibilities is dependent on the amount of unique objects we are able to design and create. Players who don’t reach the end portal in time would receive a penalty in the next minigame phase, such as obtaining half the amount of gold.

*Minigame Phase:*

Upon the end of the dungeon phase, players will enter a randomly selected competitive mini game. These games may either be free-for-all, 2 vs 2, or even 1 vs 3. There will be a lot of variety in the minigames, however many of them will contain similar underlying controls. Before each mini game would be a simple information screen for displaying the controls and goals for the mini game. Players are then given gold relative to their rankings in the game. The amount of gold obtained would be affected by multipliers the player may have gotten during the dungeon phase (e.g. x2 gold for reaching the end portal first).

The end of the minigame phase marks the end of a round. If there are still more rounds to be played, the game continues to the build phase, where the players can use the gold their obtained to make purchases if needed.

*End Goal:*

At the end of the game, the players are ranked by how much gold they have remaining: the player with the most gold is ranked first and the player with the least gold is ranked last. The goal of the game is to balance using gold to buy obstacles and structures and saving gold to win the game. There will be incentives for the players to use gold to buy obstacles: some obstacles are designed to knock gold out of other users while some obstacles are meant to stall the other players in the dungeon phase in order to reach the goal first, which increases the multiplier of the gold one wins from the next minigame. Ideally, players should be strive to win minigames and tactically place obstacles in the dungeon to their advantage. Players who are not as good at minigames can try to reach the goal first in the dungeon phase so that they will get a good amount a gold even if they don’t get first place in the minigames. They can also utilize their gold to try to knock gold off other players in the dungeon phase. Players who are good at minigames might try to spend their gold on buying items to protect themselves in the dungeon phase.

*Unique Aspects:*

It is a game that incorporates three genres: dungeon-crawling, party-game, and strategic level design. The winner of a game is never easily determined as there are many ways to turn the tables against your opponents by teaming up or strategically building obstacles. There are also multiple ways to play the game: players that are good at mini games would focus on getting the most points themselves while others can focus on stealing these points instead.

Must have:

* Variety of minigames

* Dungeon building/exploration system

* Intuitive user interface

* Interaction with obstacles and structures in the dungeon

* Currency (point) system

* Game controller input

Would be really nice:

* Cool, well-designed, and balanced structures and obstacles for the dungeon phase

* Combat system

* Cohesive art and graphics/animations

* Sound effects

* Final scoring sequence

Cool but only if ahead of schedule:

* Music / soundtrack

* More characters to choose from

* Lore and world-building / Story Mode

* Cool and fancy GUI

* Enemy AIs / COMs

* Player combat and various types of equipment

* Parameterized random dungeon generation

**Group Management**

Instead of role-based group management, each member will be responsible for their own work that has been assigned to them for that week. The group as a whole will meet often in order to take progress updates and ensure that each member is where everyone else expects them to be in terms of progress. Since everyone is having to work on implementing the project, we feel that having one or few people be the "manager" over others would be unfair.

All tasks, duties, and responsibilities are decided democratically and decisions are made based on a general vote for communal agreement. Team members can suggest ideas and volunteer to take charge of certain tasks that the rest of the team can approve of. In the event a team member would like to help take more immediate charge of delegating tasks to everyone else, final decisions are still made through group consensus.

General communication will be through discussion boards and group page, while specific discussion and major development sessions will be through in-person meetings. Clear and constant correspondence between team members will be integral during development in order to ensure thorough understanding of coding and concepts implemented during individual development.

Aside from weekly check-ins as a whole group, major milestone goals will be set up in order to check if progress is keeping up with the proposed schedule. Team members will be responsible for their individual roles for particular milestones and will notify the rest of the team should a setback occur. Members will also check in with each other to monitor if progress is moving along at a unified pace, and to ensure that each member’s perceived progress matches up with the group expectations.

If a slip in the schedule occurs and the development is behind schedule and/or becomes delayed, team members will work together to help bring the entire project to its intended checkpoint and remain on schedule. Since the group is split into focus groups (graphics/art/network) it will be easy for members of a focus group to cover for other members in the same group.

**Project Development**

*Graphics Team (Rendering, Game logic):*

* Kavin Srithongkham

* Varanon Austin Pukasamsombut

* Joshua Tang

*Networking Team (Server/Client) :*

* Ethan Chan

* Richard Lin

* Daniel Lee

*Artist (Concept Art, 3D Modeling):*

* Christiane Pham

Our development roles are divided into teams.  The graphics team has 3 members, and each will work on various graphics-related tasks on their own feature branches, and will code review each other’s changes.  Likewise, the networking team has 3 members and will function in the same way.  The gameplay and physics will likely be developed by all software group members.  As a result, our team does not necessarily have a hierarchy, as each developer’s roles are equal weighted in responsibility and power.

As for software tools, we plan to use OpenGL as our graphics library with Assimp as a support library.  We are currently developing a game engine in C++ to use in conjunction with this.  For networking, we are looking into Boost library’s ASIO for handling our server-client communication.  We also plan to use Blender for generating models. For organization tools, we will be using Git for version control and using Trello for task tracking.

We plan to write unit tests to ensure correctness of functionality as we continue development.  We will run these tests before merging in feature branches to ensure that our master branch is always stable.  Additionally, we plan to set up continuous integration to streamline the testing process.

For internal group documentation, we will be writing descriptive comments within the code to make it easy for team members to follow.  The comments will allow for a formal process for merging in feature branches, where a reviewer can read the code and comments to ensure correctness.  We believe that more sophisticated documentation (e.g. generating pages of code documentation) is overkill, given our small team size and the fact that most members will be focused on specific areas of the codebase.  For external player documentation, we plan to continuously update a "game manual" to keep track of various game features such as controls, gameplay, strategies, etc.

**Project Schedule**

Week | Graphics | Networking | Game Engine | Gameplay | Sound & Art
--- | --- | --- | --- | --- | ---
1 | Basic Setup | N/A | Basic Setup | Game Ideas | N/A
2 | Loaders for 3D models and textures, structure for low-level logic | Investigate C++ networking libraries, basic client-server interaction, initial protocol design | Structure of all systems in place. | N/A | Develop and decide on an art style.
3 | Loaders for animations |  | Smooth rendering pipeline, physics, game controller inputs | Build phase structure, initial dungeon design | Concept art for dungeon, concept art for minigames
4 | General user interface | Optimization of protocol | Control and camera modules for minigames | Minigame structure, obstacle and Structure Design | Record basic sound effects, character design, obstacle and structure design
5 | Organization and polishing of all low-level logic |  | Integrate basic sound effects into game |  | Art assets for level, record other sound effects, start music/soundtrack production for dungeon (if ahead of schedule)
6 |  |  |  | Finalization of game flow | Soundtrack production (continue)
7 |  |  |  |  | Soundtrack production (for minigames)
8 |  |  |  | Content Generation, minigame polishing | Polish art assets, polish sounds
9 |  |  |  | Alpha testing |
10 |  |  |  | Beta testing |


Key Milestones (from highest to lowest priority):

* Set up basic server/client communications

* Set up essentials of game engine

* Functionality of the build phase of the game (rendering and functionality of the build UI as well as functionality of placing tiles/constructs into the map)

* Functionality of the dungeon crawling phase of the game (transition from what is built in the previous phase to interactive gameplay into the next phase, player movement and interactivity with the dungeon, game flow of starting the dungeon to players reaching the end with events in between).

* Functionality of minigames, including easy additions of new games.

* Integration of all phases of the game, including the start menu and end scoring phase.

* Addition of all aesthetics, such as character models, animations, sounds, and effects.
