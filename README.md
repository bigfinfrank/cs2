# [Fin](https://steamcommunity.com/id/bigfinfrank)'s [CS2](https://store.steampowered.com/app/730/CounterStrike_Global_Offensive) [Autoexec](https://developer.valvesoftware.com/wiki/Autoexec).[CFG](https://developer.valvesoftware.com/wiki/CFG) and more

This is the config I use whenever I play CS2, changing game settings and console variables to match my personal preferences, make quality-of-life changes, and tweaking values for subtle competitive advantages.

## What is a `.cfg` file?

There are official Valve docs [here](https://developer.valvesoftware.com/wiki/CFG), but in short; it's a text file with a long list of console commands, typically with some blank lines for organisation and some comments that are ignored by the game but help humans understand what different parts of the `.cfg` file are for.

## What makes yours so special?

I tend to be a bit of a control freak when it comes to my games, especially the fine details and tweaking extremely minor things to my liking and to provide a competitive advantage. Since I'm extremely passionate about CS, I've spent a lot of time fine tuning as many options in game as I can and learning the inner workings of the game to the best of my abilities.
I've also spent a lot of time looking through information and posts created by the community with creative things to do with configs.
Since this is my personal config,I've made it easy for myself (and by proxy, anyone else that uses it) to have everything you could want to change organised and documented with comments, with a lot of fun and complicated tweaks that most people on CS don't even know you can do without cheats. Here's an (probably in-)complete feature list:

- Automatically set Steam group on game start up so you can join your primary group's group-exclusive server.
- Optimize networking settings for security and performance, slightly reducing network lag and overall giving you a smoother performance by letting your game utilize your internet connection to the best of it's abilities.
- Apply your favorite viewmodel every time you launch, letting you tweak your gun appearance to take up less of your screen for a competitve advantage, or shift it around to show off your brand new Battle-Scarred P250 Sand Dune.
- Change your graphics settings to minimize artifical limits on your FPS and avoid power saving modes intended for laptops and portable PCs.
- Save more information about your game and the lobbies you're playing in to look back at in the future, prove your innocence in community servers, and troubleshoot issues you run into with CS.
- Make frequent console commands easier with shorthand aliases like `nc` instead of `noclip`, `dc` instead of `disconnect`, and others.
- Temporarily up max your sensitivity while planting the bomb so you can spin extremely fast making yourself harder to hit, without needing to press a DPI button on your mouse (which also means if you get peaked while planting all you have to do is let go of the spin button, you don't need to press your DPI button again).
- Automatically show more detailed information about your movement speed, FPS, and networking information when you open up the scoreboard and hiding it away when you close the scoreboard to keeping your screen tidy of unnecessary information when you don't need it, but just a keypress away when you do.
- Automatically inspect your new Navaja Rust Coat every time you pull it out to show off to your friends.
- Perfectly crouch jump every single time, without letting your normal crouch key or human error mess anything up.
- Easily bind something to *every* key, letting you perform actions extremely quickly and often.
- Hold down on your interact key to change your scrollwheel to interact with doors extremely fast making it difficult for your opponents to hear and potentially impossible for them to get through the door in last alive bomb site situations like on Nuke or Cache.
- Easily drop yourself Vanilla versions of your favorite knives, danger zone items, and more with simple console commands. From getting your hands on a CT knife while playing as a Terrorist, to bump mines from danger zone, to a Karambit.
- Increase your volume while slow-walking to hear the sounds around you and know exactly when the enemy starts leaving an area so your team can rush in and take them off guard.
- Easily paste multi-line copy pastas and ASCII art into chat with all with one key.
- Quickly and simply change between different tickrate servers, letting you bump your tickrate up or down depending on the third part servers you're using.
- Null cancelling movement letting you immediately start going left by pressing your `+moveleft` key, without needing to let go off your `+moveright` key first making your split second movement changes harder to predict and counter.
- Quickly get any all in game actions unstuck with a single command.
- Post all of your current binds to the in game console in a straightforward, organised layout to share and compare with others.
- Automatically cycle through your clan tags whenever a key is pressed. People will be wondering how you're doing it while playing and you can rest assured that it uses a safer method of clan tag changing compared to the traditional method of binding forward, back, left, and right to their own exclusive clan tags.
- Additional viewmodel presets giving you more options to quickly change between in a pinch when you're mid game and feeling off.
- Automatically enable a longer crosshair, expanding the pips to the edges of the screen so you can easily line up precise grenades with precision.
- Togglable network "lag switch" letting you temporarily cap your game's bandwidth so you can appear stuttery and harder to hit in low health 1v1 situations.
- Single-press buy binds to buy a full rifle/AWP loadout instantly.
- Optionally disable scrollwheel jumping while shooting to retrain yourself to avoid panic jumping at the end of your Silver 1 gunfights.
- Automatically RGB spectrum cycle your crosshair, or cycle your crosshair in sync with your HUD which can also cycle through the colors of the rainbow.
- Simple anti-afk bind to type into console during warmup and easily turn off during round 1 freeze time.
- Customize the minimap radar exactly how you like it and provide the most visiblity of the map that you can.
- Save your crosshair settings exactly, including ones that aren't saved with the built-in crosshair codes feature.
- Sync your AWP zoom sensitivity with that of your rifles for more consistent flicks.
- Precisely set your sensitivity so you can always match it no matter that PC you're using.
- Disable the hints system intended for new players to learn the game, keeping your screen clear of distractions and unnecessary sounds.
- Edit all of your binds quickly and easily, keyboard row by row, including weird keys from num lock to Windows super keys.
Change the HUD just how you like it, letting you get your perfect balance between screen space and information.
- Improve your privacy, safety, and security with settings designed to keep unwanted players out of your parties, keep your game free of unnecessary toxicity, keep inappropriate user generated content off of your stream, and prevent convicted cheaters from joining your private matches.
- Customize your volume levels so when you start playing CS on a new computer, your ears will already be saved from the notorious menu music.
- Reduce audio latency, giving you a better chance at stopping a sneaky enemy just in the nick of time.
- Autocorrect for CS making sure that when you decide to leave a lobby or close the game, a rushed typo won't get in your way, your unbroken monitor will thank you.
- Included practice config with everything you could want while practicing in official matches solo or with your team.
- Included tournament config to let you and your friends play in a safe, far, and easy to set up competitive setting with just two commands.
- Fixed controller support with greater support compared to the Valve default settings.
- Easily get a list of teleportation commands to get to specific parts of maps. You can use them just to get around quickly or for KZ practice on official maps so you don't have to noclip back after messing the vent hop 10 times in a row.
- Quick reference lists for other console commands such as game_mode, game_type, and give.
- And a bunch of other miscellaneous tweaks and optimizations to ensure you're playing at the best level you can be.

## I'm new to this, why would you want a custom config??

Automation and ease of use:

- Scenario 1: **A close trusting friend of mine bought a Karambit but has a low res monitor, they want me to enter a private server with them and take screenshots on their account, but I have different keybinds.** Instead of changing all of my bindings to be able to move around manually, storing keybinds in a config let's you easily apply to them to any account you're using.
- Scenario 2: **You bought a brand new computer with all new parts and need to fresh install CS.** Instead of fine tuning all of your game settings and keybinds, having to go back and forth between your old and new PC, you can just type "exec autoexec" in console and change everything to exactly how you remember it.
- Scenario 3: **You use a bind that's more complicated than something as basic as `bind MOUSE1 +attack` like a simple crouch jump bind, requiring you to run some console commands to get it working every time the game launches.** Since all the commands in your `autoexec.cfg` file are run every time the game starts, you can just hop straight into a match and your
- Scenario 4: **You change a lot of settings in CS and like tweaking values a lot.** Using a config will let you organise the different changes you make into neat categories and easily look through complicated and/or long lists of commands you run to customise your game.
- Scenario 5: **You want to create something more advanced than a basic bind, but doing everything directly through the console is confusing**. Using cfg files lets you run console commands without the console itself, you can type out and edit commands in your favorite text editor and simply launch the game to apply your changes or bind a key to run your `.cfg` file even mid-game.

## Well how do I get set up?

It's a little daunting at face value, but in reality it's pretty simple to set up your own from scratch or use mine as a base.

1. First, go to this folder `C:\Program Files (x86)\Steam\userdata`, if you have the Steam client itself installed on a different drive, find your `Steam` folder and then find `userdata` within it.
2. If there's only one folder with a bunch of numbers, enter that one. If you have multiple, you can find the number that's associated with your account in your [trade URL](https://steamcommunity.com/id/bigfinfrank/tradeoffers/privacy#trade_offer_access_url), look for the numbers between `?partner=` and `&token` in the URL and they should match up with one of the ones in your userdata folder.
3. Find the folder with CS's App ID, `730` and open it, inside `730`, open `local`, and inside `local`, open `cfg`. If you look at the top bar in File Explorer, your folder structure should look something like this `C:\Program Files (x86)\Steam\userdata\123456789\730\local\cfg`.
4. Either download this GitHub repository and drag the files into this `cfg` folder, or create a new plain text file called `autoexec`, and change the extension from `.txt` to `.cfg`, CS automatically looks for this file when you launch the game and runs the commands within it.
5. Open up the file and type in `clear; echo My first autoexec just got executed!`, then start up the game.

- If you open up the console and scroll to the very top, you should see text saying `My first autoexec just got executed!` and that means you're good to go! Start putting console commands you run in game into your `autoexec.cfg` file and they'll automatically be run every time you launch CS.
- If you don't see it, double check you spelled everything right and try typing `exec autoexec.cfg` in console, then:
  - If it says the file doesn't exist, you probably put the file in the wrong folder, or didn't change the extension correctly.
  - If it clears your console and shows the text, but doesn't do so when the game launches, add `+exec autoexec.cfg` to your [launch options](https://help.steampowered.com/en/faqs/view/7D01-D2DD-D75E-2955) for CS, and try again.

## Is there anyting else to customize after I've got my config set up?

There's always more you can do. A few popular ones are:

- [VibranceGUI](https://vibrancegui.com) lets you increase the vibrancy of colors in CS across all maps and UI.
- [Simple Radar](https://readtldr.gg/simpleradar) removes unnecessary clutter from the minimap and provides cleaner, more distinct outlines of areas on the map.
- [Improved Radio Mod](https://maximhere.me/modifications) changes the default radio menus to include more options and toggles for some common commands like noclip.

### Launch options

Separate from the above list of plug-and-play tweaks, you can also change your game's launch options to enforce certain settings and help CS behave as you'd like it to on your system, remove some artificial limitations, and add some functionality. Mine are below, along with short descriptions for each of them:

- `-small` Allow window sizing smaller then 640x480
- `-dev` Enables developer mode. Also disables the automatic loading of menu background maps and stops the quit dialog from appearing on exit.
- `-high` Sets the game's priority to High
- `-d3d9ex` Reduce CPU memory about %40. "csgo" only. (Rumored to be purely placebo, but doesn't cause any harm to include it)
- `-forever` When you get to the end of the maplist, start over from the top, keeping a game server open indefinitely.
- `-novideo` When loading a game with this parameter, the intro video will not play.
- `-nojoy` Disables joystick (controller) support. Theoretically slightly reduces memory usage and fixes a thread starvation lag spike isuse.
- `-threads 16` Number of threads to allocate for the thread pool, default is 3. Set this to the number of CPU threads your CPU has, up to 16. Above 16 caused random inconsistent crashes on CSGO after playing for a while, so until it has been tested you should assume that values above 16 will also crash CS2.
- `-nogammaramp` tells CS to use your monitors brightness instead of the in-game brightness level set by yourself.
- `-language fin` Changes your language to a custom one, mine is a modified version of [Maxim's](https://maximhere.me/modifications).
- `-rpt` Same as having -condebug, -conclearlog, and -console enabled
- `-refreshrate 165` Force a specific refresh rate (set this to your monitor's refresh rate)
- `-vcrrecord latest.vcr` Records a client's game and allows you to play it back and reproduce it exactly.
- `-tickrate 128` Specifies Server-Tickrate (for more info see Source Multiplayer Networking).
- `-fullscreen` Forces the engine to start into exclusive fullscreen mode.
- `-windowed` Forces the game into windowed mode
- `-noborder` Forces the window to be borderless (used in combination with -windowed for Borderless Windowed)
- `-pakxv_lowviolence` Changes blood decals to black instead of red
- `-maxplayers_override 255` Specifies how many player slots the server can contain.
- `-maxdownloadfilesizemb 32768` CS:GO 5/1/2014, client launch option -maxdownloadfilesizemb N if clients needs to download even larger files from community servers.
- `+exec ./autoexec.cfg` Executes specific config file immediately after the engine is loaded.
Or in a single copy & paste-able codeblock:

```txt
-small -dev -high -d3d9ex -forever -novideo -nojoy -threads 16 -nogammaramp -language fin -rpt -refreshrate 165 -vcrrecord latest.vcr -tickrate 128 -windowed -noborder -pakxv_lowviolence -maxplayers_override 255 -maxdownloadfilesizemb 32768 +exec ./autoexec.cfg
```


small has been removed.
d3d9ex has been removed.
forever has been removed.
novideo has been removed.
nojoy has been removed.
nogammaramp has been removed.
rpt has been removed (subsequently, conclearlog has been removed as well)
refreshrate has been removed.
vcrrecord has been removed.
tickrate has been removed.
windowed has been removed.
pakxv_lowviolence has been removed (experimenting with forcing perfectworld)
maxplayers_override has been removed. (no maxplayers either)
maxdownloadfilesizemb has been removed.


Experimental migration values:
```txt
-dev -devcontent -threads 16 -language textmod -condebug -console -noborder +exec ./autoexec.cfg
```

favor_consistent_framerate should be experimented with (better fps stability for free?)
set_power_qos_disable should be experimented with (force disable of in game power optimisation)
forcenovsync should be experimented with (force disable of vsync graphics settings)


## To-do List

These are eventual features that don't have a great effort to benefit ratio for my personal use cases, but I'd like to include eventually.

- Make necessary changes for the config to work flawlessly in CS2, removing broken features and making adjustments where necessary.
  - A state-reset script might be useful in keycontainer, see fin_uninspect
- External GitHub Wiki documentation.
- Move CS2 config to it's own repository OR move TF2 and CSGO configs out of this repository.
- Implement [MrMaxim's "ADVANCED BIND SCRIPT"](https://www.youtube.com/watch?v=xVrFxYeSJ7Q) allowing you to bind multiple separate actions to the same key and only executing certain actions if a modifier key is held
- Verify that the `S1_UP` and `S2_UP` keys map to releasing stick buttons on controllers.
