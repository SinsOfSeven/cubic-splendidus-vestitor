# 3Dmigoto-Tailor
This tool is designed to solve the problem in DarkStarSword's blender-3dmigoto.py plugin:

"Only draw calls using a single vertex buffer and a single index are supported now"

This tool is used in 3Dmigoto dump files which use higher vertex buffer slot,
for example some game only use vb0 to store all information like {Dead or Alive},
but other games use vb0,vb1,vb2,etc..,Unity game normally use vb0 to store POSITION,NORMAL,TANGENT info,
use vb1 to store COLOR,TEXCOORD info ,use vb2 to store BLENDWEIGHT or BLENDWEIGHTS, BLENDINDICES info,
and for UE4 it's more complicated,so if you need to use 3Dmigoto-Blender plugin from DarkStarSword's github
to import these dump file into blender, you will need to first merge these vb0,vb1,vb2 into a single vb0,
that is why I created 3Dmigoto-Tailor to do this,because manually do this will take a lot of time.

And 3Dmigoto-Tailor is designed to compatible with as many games as it can,so it's a little bit complicated
to use,but if you have some patient to read the code,you will know this tool can save a lot of time for you,
and is very simple to use once you understand the config file architecture.

But use 3Dmigoto to mod game is only restricted on GPU Driven Animation Game,so only part of the games 
can use 3Dmigoto, and most of them use Higher buffer slot tech,and Tailor can handle this.

in addition,there is so many useful sctipts,like AnalysisScripts used to do analysis on FrameAnalysis folder,
like FormatConvert to convert a mod into .ib and .vb file, etc...

Notice: This tool is designed for shader hackers, it may take some time to read the code to know how config work.

# Features
- You can use this tool to make all paid mod,you can do whatever you want for any mod made with this tool,
you don't have to turn you mod into free after 30days like AGMG rules,just do what you want to do.
- Support as many games as it can by simply add the config file for new game.
- Support both R16_UINT and R32_UINT format.
- You can reverse other people's mod with scripts in FormatConvert folder, it can turn a producted mod into original
.ib and .vb format, and then you can import it into blender and modify it
(removed due to modder's copyright or credit reason, you can ask me to get it when you get ProModder identity 
in AGMG discord community).

# Design
 - One time only extract one Index Buffer, because only process one is already easy to get error,
more than one part will be very hard to debug, I have test it a long time before,seems not good, so only
process one IB in one time.
 - After .ini file generated, you need to manually modify it to let it work well,because what generate is
just a example .ini file, not the final .ini file, you need to modify it yourself.
 - You have to use DarkStarSword's blend-3dmigoto plugin, which I have already put them in Plugin folder.

# TODO list
 - UE4's BINORMAL problem ,this problem is exists in UE4 game ,like KALABIYAU,SNOWBREAK,BLUEPROTOCOL etc.
and there is a normal is 4D problem I have already solved,but the rest part BINORMAL or BITANGENT problem still need 
to test and solve.
 - add dynamic mod support.
 - add GUI mod manager support.
 - add Mod merge scripts to combine mod.
 - add scripts to make toggle mod. 

# GPU Driven Animation Games
 - Honkai Impact 3 
 - Honkai Star Rail 
 - Genshen Impact 
 - Naraka Bladepoint 
 - Kena Bridge Of Spirit 
 - KALABIYAU 
 - BLUE PROTOCOLS 
 - SNOWBREAK 

# Community
https://discord.gg/gEzkrsvJCt

Join this discord for:
- Technique support
- bug-report
- advice and feedback
- Other


# Acknowledgements
Without their original 3dmigoto repository the 3Dmigoto-Tailor repository is meanless. 
Huge thanks to Chiri,DarkStarSword,bo3b and 3Dmigoto original author group.

Special thanks for GIMI&SRMI author: SilentNightSound



