---
layout: post
title:  "Farming Simulator Updates, how to fix your mods"
date:   2022-10-26
excerpt: "Updates to Farming Simulator 22 can be breaking, here's how you can fix some yourself!"
feature: https://i0.wp.com/waytoomany.games/wp-content/uploads/2021/12/Farming-Simulator-22-Cover-Image.jpg?w=2560&ssl=1
tag:
- farming
- simulator
- 2022
- modding
- open 
- source
comments: true
---

> Help! Mod X is broken!

## Update process

When Giants updates the base game they can make mods break. This is because the mods often overwrite certain methods or they check against
global variables set. So when those variables are changed and your mod is still checking against that old value it will not work anymore with the new version.
Likewise, when you change your mod code to reflect the new status quo at Giants, people who haven't updated the game, but do update your mod will also have a problem.
The best way to mitigate this is by versioning your mod as well and write clear changelogs.

## Lumberjack

I frequently use the Lumberjack mod, mainly for their superstrength and also a bit for cutting tree stumps. On the day of the `v1.8.1.0` patch I installed it and realised my super strength wasn't working.
PANIC! Because I had a tractor/trailer combination stuck on top of one of my greenhouses... 😬. I did not want to reset the vehicle because I didn't want to drive back from the store and also not lose what was in the trailer!
So I thought, this must be fixable! 

## Local editing of mod files

Every mod's code is publicly available, since you can just unzip the mod file and see the files. Nothing is encrypted. Some mods even upload their code to Github so you could view the code there as well. 
So here's how to get to edit the code locally so it loads into your game as well.

1. Go to your mods folder and locate the .ZIP file of the mod you want to edit.
2. Click right mouse button and select "Extract all"
3. Make sure to extract it in the same folder your mods are in
4. You now should have a folder with the same name as the .ZIP file in your mods folder
5. Open or download a code editor. Notepad will work, but for some nice features that help the code be more readable I would advise using [Visual Studio Code](https://code.visualstudio.com/download).
6. Within your code editor open the folder with the mod files you just extracted.

For me it looks something like this:
