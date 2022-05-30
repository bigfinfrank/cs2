# [Fin](https://steamcommunity.com/id/bigfinfrank)'s [CSGO](https://store.steampowered.com/app/730/CounterStrike_Global_Offensive) [Autoexec](https://developer.valvesoftware.com/wiki/Autoexec).[CFG](https://developer.valvesoftware.com/wiki/CFG) and more

This is my CSGO "Config" or as I prefer to call it, my CSGO autoexec. It's what customises my game beyond what the in-game settings UI lets you using automatically run console commands. By design, because you can use it to run any in-game console command as if you opened the console and typed it in, this is insanely powerful.
One simple example is the (now patched?) CSGO bomb finding bind that turns on the game instructor (the tutorial-esque popups) to show where the bomb is through smokes.


## You lost me at "Autoexec"
That's totally fine, it's definitely complicated (especially for beginners) and creating your own can be pretty daunting. I'll do my best to use simple and uncomplicated terminology in the explanations below, just please try not to get turned away by the size of the CFGs.
There's a lot in them but it all breaks down to some pretty simple formatting and everything is organized (and soon documented on each line)


### CFG Explanation
CFG is a file type just like `.exe` or `.txt`. When you put a file ending in `.cfg` (i.e. `autoexec.cfg`) in specific folders, CSGO will see that and know that the file has console commands.
If you're more technically inclined, Valve has a more detailed explanation of these files in their Developer Docs which you check out [here](https://developer.valvesoftware.com/wiki/CFG).


### Autoexec Explanation
Autoexec's are files named `autoexec.cfg` that you have to manually add to one of the game's `cfg/` folders. They're files that CSGO will look for when the game starts and run the commands inside. This lets you automate changing settings, quickly share all of your settings with others, and accomplish some really awesome automation & tricks by using the game's console to our advantage.
If you're more technically inclined, Valve has an explanation of these files in their Developer Docs which you check out [here](https://developer.valvesoftware.com/wiki/Autoexec).


Still have questions? Check the FAQ below and if you still don't have an answer, create an [Issue](https://github.com/bigfinfrank/cfg/issues) and ask me your question!


## FAQ
- **My autoexec isn't working!**
  Make sure you have `+exec autoexec.cfg` in your [launch options](https://support.steampowered.com/kb_article.php?ref=1040-JWMT-2947) for CSGO
- **Do I need to use any other launch options?**
  While you don't *need* to, you can get some extra functionality and potentially performance from some launch options. See the Launch Options section below.


## Launch Options
Launch options are options you can set that the game will use when it loads.


### What launch options do you use?
Mine are specifically setup for my PC (**Seriously, if you use mine exactly you could run into game crashes and screen tearing**), to make it easy there are mine and a freely copy-pastable version below mine. These will look complicated at first but they all just change one thing each so it's not that complicated.

Mine:
```code
-small -forever -novid -language fin -rpt -vcrrecord -tickrate 64 -windowed -noborder -maxplayers_override 255 +exec ./autoexec.cfg +joingame
```
Mine without the PC-specific options (easy copy-paste):
```code
-small -forever -novid -language fin -rpt -vcrrecord -windowed -noborder -maxplayers_override 255 +exec ./autoexec.cfg +joingame
```

First to get this out of the way, options that start with a `-` are "normal" launch options that change stuff about how the game launches, tell the engine to do a certain thing, or hint to your OS about something. The ones that start with a `+` are simply in-game console commands that will be run as soon as the game starts.
One example of where this could be useful is if you needed to use sv_cheats commands in your autoexec, you could put `+sv_cheats 1` in your launch options and turn off sv_cheats at the end of your autoexec that way the cheat command is enabled when you launch but if you reload your config in-game it won't disable achievements.


### How do I set launch options?
To change your launch options for steam games, the best and easiest way to change these is to:

1. Go to your steam Library
2. In the list of games on the left side of the window, right click the game that you want to change the launch options of
3. Click "Properties..."
4. Click the "GENERAL" tab on the left of the popup window
5. Put your launch options in the "LAUNCH OPTIONS" textbox at the bottom of the popup window


### What does each option do?

- `-d3d9ex` Supposedly "reduce CPU memory about %40. 'csgo' only." There was some talk about it being placebo but here's [evidence that says otherwise](https://imgur.com/a/gnEqTT0) from the CSGO source code leak. **You shouldn't need to change this**
- `-threads 16` This is the number of threads that CSGO should use, a CSGO dev recommends against setting this but I do anyways. **You need to change this** You can either remove it which is what CSGO developers say you should do, otherwise: Don't set it above 16 (otherwise the game crashes randomly) and don't set it above your CPU's thread count.
- `-small` Removes minimum 640x480 size window size limit for CSGO, this only affects really tiny custom resolutions and windowed mode users who feel like making it so they can't see their game. **You shouldn't need to change this**
- `-novid` Skips the golden "CSGO" loading text that shows up when you start the game, this can lead to faster game start up times if your computer is fast enough because in some cases the Main Menu will already be done loading and just sitting their waiting for the CSGO logo animation to fade out before the menu pops up.
- `-language bigfinfrank` This sets the game to use my custom language (based on BananaGaming's Text Color Mod). **You might need to change this** if you use a non-English language in CSGO. If you want to use my language changes, move `csgo_bigfinfrank.txt` to the `Counter-Strike Global Offensive\csgo\resource` folder.)
- `-rpt` "Same as having -condebug, -conclearlog, and -console enabled". -condebug: Logs all console output into the console.log text file. -conclearlog: Clears the console.log text file on start. Only works if -condebug set. -console: Starts the game with the developer console enabled. Same as having con_enable enabled. **You shouldn't need to change this**
- `-vcrrecord` "Records a client's game and allows you to play it back and reproduce it exactly." This effectively records a client-side demo that you can play back later. This provides more accurate gameplay (and maybe higher tickrate?) than Valve matchmaking demos because it's recorded directly on your PC. **You might need to change this** if you are really stretched thin on performance.
- `-tickrate 64` This sets your game's default tickrate to 64. **You might need to change this** if you're playing on higher tickrate servers, for example I believe FACEIT and ESEA use 128 tick servers, so you'd want to set this to 128 instead.
Theoretically you could get a slight advantage by setting this above the server you're playing on's tickrate because the client and server don't actually sync up and that means that you're checking for updates from the server more often could give you an ever-so-slight advantage (but we're talking about miliseconds here).
- `-high` Launches the game with the "high" priority in Windows. To put it simply, this hints at windows that it should make CSGO a priority over other programs. **You shouldn't need to change this** but if you're having Discord stop responding or something and you'd rather have a bit lower performance, go ahead and
- `-windowed` Launches the game in windowed mode, **You might need to change this** if you're using a resolution that isn't your monitor's native one as in most cases you need to be using fullscreen for custom resolutions.
- `-noborder` Launches the game without a window border, **You might need to change this** if you're using a resolution that isn't your monitor's native one as in most cases you need to be using fullscreen for custom resolutions.
- `-refreshrate 144` Forces the game to use a certain refresh rate, you should always set this to your monitor's refresh rate, don't use this as a framerate limiter, use fps_max and fps_max_menu instead. **You probably need to change this** if your monitor's refreshrate isn't set to 144hz in Windows.
You can check to make sure that you have manually set it (which you need to do on high refresh rate monitors) and that Windows didn't randomly revert it by opening the Settings app, going to Display -> Advanced display -> and making sure Choose a refresh rate is set to the highest it can go to, the number will probably not be a whole number so just round to the nearest one.
- `-maxplayers_override 255` This sets the maximum players that can be in servers you host to 255 which is the absolute maximum set by the Source Engine. CSGO has it's own limitation that limits this to 64 and without editing `botprofile.db`, `gamemodes.txt`, and `gamemodes_server.txt.example` you can't get above 42 (bots). **You shouldn't need to change this**
- `+exec ./autoexec.cfg` This executes autoexec.cfg, this shouldn't be necessary but unless you've done some really weird and exotic modifications it doesn't hurt anything to have it run twice.


## Todo List
*Help with these would be much appreciated*

+ Implement [BananaGaming's "ADVANCED BIND SCRIPT"](https://www.youtube.com/watch?v=xVrFxYeSJ7Q&t=0s) (multiple binds per key using key combos)
+ Figure out what the `S1_UP` and `S2_UP` keys map to physically on controllers
+ External doumentation (with GitHub Wikis)
