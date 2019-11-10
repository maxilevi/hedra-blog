---
layout: post
title:  "Weekly Update #3: Dungeons & NavMeshes!"
date:   2019-11-10
author: Zaphyk
---

This week's most of my efforts where focused in adding more content into the game. More specifically I worked on adding a new dungeon into the overworld. Here is a picture of the model:

![](/assets/img/post2/dungeon_blender.png)

Here is a picture of the inside layout:

![](/assets/img/post2/dungeon_layout.jpg)

So adding the model and the collisions into the game was pretty easy and performant because of groundwork that was done a few months before. (This "groundwork" was porting the engine to use [bulletphysics](https://en.wikipedia.org/wiki/Bullet_(software))). Here is a picture of the dungeon ingame:

![](/assets/img/post2/ingame0.png)

Instead, the development bottleneck was making the AI work smoothly. Currently the AI for the mobs uses [A*](https://en.wikipedia.org/wiki/A*_search_algorithm) which is an algorithm for finding a shortest path from a grid of points. This works fine in the overworld terrain however when mobs are inside structures there are too many grid points to sample so the AI becames too slow to do anything.

My first idea for solving this issue was to use [navigation meshes](https://en.wikipedia.org/wiki/Navigation_mesh) this would allow me to clearly define "walkable zones"
that the AI can traverse. Then I would build a [graph](https://en.wikipedia.org/wiki/Graph_theory) out of those "walkable zones" and use it as waypoints.[0] Here is an ingame picture:

![](/assets/img/post2/navmesh.png)

Now finding shortests paths isn't something very hard to do since it's well explored topic. For solving this particular problem I used [Dijkstra's algorithm ](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)

Here is a simple explanation from [wikipedia](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm):

_Suppose you would like to find the shortest path between two intersections on a city map: a starting point and a destination. Dijkstra's algorithm initially marks the distance (from the starting point) to every other intersection on the map with infinity. This is done not to imply that there is an infinite distance, but to note that those intersections have not been visited yet. Some variants of this method leave the intersections' distances unlabeled. Now select the current intersection at each iteration. For the first iteration, the current intersection will be the starting point, and the distance to it (the intersection's label) will be zero. For subsequent iterations (after the first), the current intersection will be a closest unvisited intersection to the starting point (this will be easy to find)._

![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Dijkstra_Animation.gif/220px-Dijkstra_Animation.gif)
Source: [1]

That's all!

Notes:

[0] This is basically applying A* but on graph thats not build in realtime.

[1] https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm
