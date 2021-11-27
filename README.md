# [Fin](https://steamcommunity.com/id/bigfinfrank)'s [TF2](https://store.steampowered.com/app/440/Team_Fortress_2/) [Autoexec](https://developer.valvesoftware.com/wiki/Autoexec).[CFG](https://developer.valvesoftware.com/wiki/CFG) and more

This is my TF2 "Config" or as I prefer to call it, my TF2 autoexec. It's what customises my game beyond what the in-game settings UI lets you using automatically run console commands. By design, because you can use it to run any in-game console command as if you opened the console and typed it in, this is insanely powerful.
One simple example is the (now patched?) TF2 bomb finding bind that turns on the game instructor (the tutorial-esque popups) to show where the bomb is through smokes.

I should also point out that the main files (no custom knife files or anything) as well as my launch options and my settings are available nicely formatted on [settings.gg](https://settings.gg/player/248313757)


## You lost me at "Autoexec"
That's totally fine, it's definitely complicated (especially for beginners) and creating your own can be pretty daunting. I'll do my best to use simple and uncomplicated terminology in the explanations below, just please try not to get turned away by the size of the CFGs.
There's a lot in them but it all breaks down to some pretty simple formatting and everything is organized (and soon documented on each line)


### CFG Explanation
CFG is a file type just like `.exe` or `.txt`. When you put a file ending in `.cfg` (i.e. `autoexec.cfg`) in specific folders, TF2 will see that and know that the file has console commands.
If you're more technically inclined, Valve has a more detailed explanation of these files in their Developer Docs which you check out [here](https://developer.valvesoftware.com/wiki/CFG).


### Autoexec Explanation
Autoexec's are files named `autoexec.cfg` that you have to manually add to one of the game's `cfg/` folders. They're files that TF2 will look for when the game starts and run the commands inside. This lets you automate changing settings, quickly share all of your settings with others, and accomplish some really awesome automation & tricks by using the game's console to our advantage.
If you're more technically inclined, Valve has an explanation of these files in their Developer Docs which you check out [here](https://developer.valvesoftware.com/wiki/Autoexec).


Still have questions? Check the FAQ below and if you still don't have an answer, create an [Issue](https://github.com/bigfinfrank/cfg/issues) and ask me your question!


## FAQ
- **My autoexec isn't working!**
  Make sure you have `+exec autoexec.cfg` in your [launch options](https://support.steampowered.com/kb_article.php?ref=1040-JWMT-2947) for TF2
- **Do I need to use any other launch options?**
  While you don't *need* to, you can get some extra functionality and potentially performance from some launch options. See the Launch Options section below.


## Launch Options
Launch options are options you can set that the game will use when it loads.


### What launch options do you use?
Mine are specifically setup for my PC (**Seriously, if you use exactly you could run into game crashes and screen tearing**), to make it easy there are mine and a freely copy-pastable version below mine. These will look complicated at first but they all just change one thing each so it's not that complicated.

Mine:
```code
-d3d9ex -no_texture_stream -small -forever -novid -rpt -tickrate 32 -high -windowed -noborder -refreshrate 144 -maxplayers_override 255 +exec autoexec.cfg
```
Mine without the me-specific options (easy copy-paste):
```code
-d3d9ex -no_texture_stream -small -forever -novid -rpt -tickrate 32 -high -windowed -noborder -maxplayers 255 +exec autoexec.cfg
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
- `-threads 16` This is the number of threads to allocate for the thread pool, [a Valve Employee recommended against setting this on reddit](https://www.reddit.com/r/GlobalOffensive/comments/5y8r7v/comment/dep5yno) but I do anyways. Don't set it above 16 (otherwise the game crashes randomly after a while) and don't set it above your CPU's thread count.
- `-small` Allow window sizing smaller then 640x480, you shouldn't ever go below that resolution but this will *let* you, with some potentially interesting UI consequences.
- `-novid` The game's "intro video will not play", this means you'll use a tiny bit less of RAM and you'll get into the main menu a little bit faster with the one con of the game being black until the main menu does load..
- `-rpt` Clears console.log on startup, logs all console output in console.log, and starts the game with the developer console enabled.
- `-high` Launches the game with [HIGH_PRIORITY_CLASS in Windows](https://docs.microsoft.com/en-us/windows/win32/procthread/scheduling-priorities), effectively hinting that it should make TF2 a priority over other programs.
- `-windowed` Launches the game in windowed mode.
- `-noborder` Launches the game in borderless windowed if the game is running in windowed mode, making it look like it's fullscreen but without the game minimizing when you click outside the window, however this will break support for stretched resolutions
- `-refreshrate 144` Force a specific refresh rate, you set this to your monitors refreshrate. Don't use this as a framerate limiter, instead you should use the fps_max and fps_max_menu console commands instead.
- `-maxplayers 255` This is used to "Set the maximum players allowed to join the server", 255 is the absolute maximum set by the Source Engine.
- `+exec autoexec.cfg` This executes autoexec.cfg, this shouldn't be necessary but unless you've done some really weird and exotic modifications it doesn't hurt anything to have it run twice.


## Todo List
*Help with these would be much appreciated*

+ Implement [BananaGaming's "ADVANCED BIND SCRIPT"](https://www.youtube.com/watch?v=xVrFxYeSJ7Q&t=0s) (multiple binds per key using key combos)
+ External doumentation (with GitHub Wikis)


## Contributing
Push a signed commit adding your name (and optionally a link to your GitHub or account on a popular social media platform) to CONTRIBUTORS.md then make a Pull Request with your changes. Afterwards you can start making Pull Requests with proper changes!
