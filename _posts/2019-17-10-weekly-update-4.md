---
layout: post
title:  "Weekly Update #4: Polishing the dungeon"
date:   2019-11-10
author: Zaphyk
---
This week development time was mostly spent on finishing the first dungeon introduced in the previous [devblog](https://blog.projecthedra.com/2019/11/10/weekly-update-3.html). This required quite a few systems to be setup and a lot of testing to be done. Hopefully it will take less time for the other dungeons!

The first thing that was done in the previous week but needed improvement was the navmeshes. The navmeshes created allowed the AI to traverse the dungeon correctly but only in ways the polygons were defined. To improve on this I raycasted the navmesh with a step so I could create a uniform grid of squares which allows more discrete steps. Here is a comparison:

![](/assets/img/post4/navmeshes.png)

I also worked on adding elements like chests, levers and torches which give life & interactiness to the building. Here are some pictures:

![](/assets/img/post4/lever.png)

![](/assets/img/post4/torches.png)

And finally I worked on adding the boss to the dungeon. Getting all the spells right and balacing was quite time consuming but definitely worth it! Here is a picture:

![](/assets/img/post4/dungeonboss.png)

Thats all for this week. Hope you enjoyed :)
