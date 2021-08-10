# [Fin](https://steamcommunity.com/id/bigfinfrank)'s [CSGO](https://store.steampowered.com/app/730/CounterStrike_Global_Offensive) [Autoexec](https://developer.valvesoftware.com/wiki/Autoexec).[CFG](https://developer.valvesoftware.com/wiki/CFG) and more

This is my CSGO "Config" or as I prefer to call it, my CSGO autoexec. It's what customises my game beyond what the in-game settings UI lets you using automatically run console commands. By design, because you can use it to run any in-game console command as if you opened the console and typed it in, this is insanely powerful.
One simple example is the (now patched?) CSGO bomb finding bind that turns on the game instructor (the tutorial-esque popups) to show where the bomb is through smokes.

I should also point out that the main files (no custom knife files or anything) as well as my launch options and my settings are available nicely formatted on [settings.gg](https://settings.gg/player/248313757)


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


## Todo List
*Help with these would be much appreciated*

+ External doumentation (through the GitHub Wiki feature)
+ Finish inline documentation (See "// TODO: " comments)
+ Add semicolons after every convar and command;
+ Implement [BananaGaming's "ADVANCED BIND SCRIPT"](https://www.youtube.com/watch?v=xVrFxYeSJ7Q&t=0s) (multiple binds per key using key combos)

* Grammar/typo check
* Change binds to use all caps (because that's how they're stored by Valve in `config.cfg`)
* Make newlines and spacing have consistent formatting

- Remove old unused stuff
- Remove broken 'features' of the config
- Remove convars and commands that Valve removed


## Contributing
Push a signed commit adding your name (and optionally a link to your GitHub or other popular social media account) to CONTRIBUTORS.md then make a Pull Request with that change. Afterwards you can start making Pull Requests with proper changes!
