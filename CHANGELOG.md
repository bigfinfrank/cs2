# Fin's CSGO Config Changelog
This file contains the changes made version-by-version from newest at the top to oldest at the bottom.
Updates prior to 1.0.15 have not been (and probably won't be) documented.
1.0.15 is the first Changelog added and has an incomplete list of changes but the changes still serve as a good example for the diff-like formatting.
New updates are added as a h2 header (`##`) above the previous version (meaning new versions will always be added to the TOP of this document). Changes to the changelog for a previous version are allowed under the condition that they must be documented in a new update (this means there will be a version bump even if no changes are made to any other files)
We use [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) which is the undoubtedly best format for version formatting, please use it for your own projects.


## 4.2.0
```diff
+ Added comments under [1.0] listing the different rate values and their bandwidth limits in kbps/mbps
+ Added functional network-only lag switch alias [3.3.19] includes a commented out version with a frame limiter as well which I don't prefer but it provides a greater effect.
+ Added fin_antiafk and fin_antiafk2 alises [3.3.26] to enable and disable an "anti-afk mode" of sorts.
+ Re-added fin_nextxhair (rainbow crosshair cycler) to fin_keycontainer
+ Added sv_reliableavatardata to prevent avatar spoofing
+ Added a "projector slide" click noise that plays whenever the config is (re-)reloaded.
+ Added "grammarly for counter-strike players", spelling-correction aliases for disconnect, exit, and quit so when you're trying to rage quit and you typo it you don't break your keyboard (more than you already have). These are stored in their respective files in ./aliases/grammarly/ and are exec'd in [11.0]

* Bindings no longer use Workman keyboard layout.
* Changed mm_dedicated_search_maxping to 135
* Changed net_graph from 2 to 1
* Adjusted FOV capitalisation so it's consistently uppercase throughout comments
* Changed fps_max_menu and fps_max from 1000 to 0 to reduce stutter caused by frame limitter overhead
* Changed capitalisation of aspectRatioWidth and aspectRatioHeight in m_yaw comment to use lowerCamelCase instead of alllowercase
* Changed overall volume levels from 0.2 and 0.25 while slow walking to 0.1 and 0.15 respectively
* Fixed +voicerecord usage on the main menu
* Fixed directory name used in [3.3.15] pointing to ./lists/ instead of ./keys/
* Fixed [3.3.11] chat aliases and fin_nextxhair, they were broken by the fin_ prefix change introduced in 4.1.2
* Revised comment for fin_clearchat with clarification for the purpose of "Damage Given" prefacing the arabic characters.
* Adjusted whitepsace for; fin_knives, fin_noknives, fin_vmpminbob, snd_mixahead, and various lines in [3.3.16], [3.3.18] [3.3.24]
* Adjusted sensitivity to match my base Valorant sensitivity of 1.0, it's a repeating decimal so I'm storing it to the greatest precision the source engine will allow.
* A few minor grammatical and 'techincally-correct' changes
* Changed MOUSE4 from fin_rifle to +voicerecord
* Changed MOUSE1 to use normal +attack instead of +noscroll_attack
* Changed some privacy & safety settings to be FaceIT friendly.
* Disabled main menu music
* Changed from borderless windowed to exclusive fullscreen
* The usual config.cfg updates
* Fixed fpsbugfix.cfg

- Removed comment about my specific ping to Sterling from mm_dedicated_search_maxping line
- Removed old comment for a work in progress one-button jump throw bind
- Removed duplicate cl_show_observer_crosshair from [8.0], can be found in [9.1] still.
- Removed cl_accountprivacysetting1 as Valve removed it at some point
- Removed cl_righthand "1"; from [11.0]
```


## 4.1.4
```diff
* Changed bindings to use the Workman Keyboard Layout (https://workmanlayout.org)
```


## 4.1.3
```diff
+ Added shorthand alias "bp" for "bot_place"
+ Crouch jump now knows if you're holding down your crouch key and won't uncrouch when you release space if you're holding down crouch.
+ Holding E now makes the scroll wheel spam +use (so you can spam open close doors really fast)
+ Grenade binds now also buy the grenade if you're in spawn and don't already have it
+ Scroll jumping is now disabled while holding left click
+ Added a (currently unassigned) rainbow crosshair set of aliases
+ 1 key is now a hold-for-knife bind
+ If you don't have a gun of a certain slot, the key will automatically equip the next best thing (ex. if you press the key to go to your primary/rifle slot, it'll go to your secondary/pistol). This is mostly useful on pistol rounds
+ Caps lock now toggles r_drawclipbrushes 2 to check if you can reach certain spots in private matches/demos.

* fin_version now echoes the response
* Moved info box over a few columns
* Updated some in-line comments
* Fixed some missing new lines
* Fixed some extra and some missing whitespace in a few comments
* Renamed some aliases
* Vertically aligned some elements
* Fixed clearchat alias not using fin_ prefix on kp_ins key
* Playercount HUD position is now at the bottom of the screen
* Hud scaling is now at exactly 0.5
* Hud color is now light blue
* Turned on demo indexing (Skipping forward and especially backwards through demos is SIGNIFICANTLY faster now).
* Disabled rcon in Privacy & safety settings
* snd_mixahead is now the exact lowest value I can have it at (with my Corsair Void Pro Wireless)
```


## 4.1.2
```diff
+ Added fin_version alias to [0.0] which can be used to print the current version
+ Added "fin_" in front of all custom aliases
+ Added "fin_visleaf", "fin_verify", and "fin_fpsbugfix" to link to documentation on how far wallhacks can see, how to verify game files, and a fix for the FPS bug that tells teammates how to fix it as well.
+ Added joingame to launch options in README.md to hopefully auto-reconenct to comp matches if you need to restart your CSGO mid game.

* Updated comments in the info box at the top of autoexec.cfg
* Changed exec commands to use more explicit paths ./
* Updated mat_queue_priority and mat_queue_mode convars to use their ideal values (see https://www.reddit.com/r/GlobalOffensive/comments/5zkpwn)
* Updated +fin_defuse alias to try and get around Valve's patch of the bomb finder
* Fixed some extra spaces in comments
* Renamed nadecrosshairoff and nadecrosshairon to nadechoff and nacechon respectively
* Fixed missing spaces between semicolons and the following convars/commands in binds
* Updated mp_respawnwavetime to use the new separate T and CT convars in practice.cfg
* Changed from 1920x1440 (1440p 4:3) to 2560x1440 (1440p 16:9 / Native) in video.txt
* Updated aliases.cfg with new .cfg's from the aliases/ folder

- Removed +inspect alias in favor of directly using +lookatweapon
- Removed _underscores_ from all aliases (leaving fin_ of course)
```


## 4.1.1
```diff
+ Added a jump throw bind (capable of left, right, and both-click throws)
+ Made jump binds smarter

* Changed noclip bind from ALT to Z.
* Fixed some missing whitespace
* Fixed comment typos

- Removed game insructor and hints toggles from +defuse.
```


## 4.1.0
```diff
+ .gitignore now ignores video.change*.txt files
+ Now sets steamgroup and clanid to a CFG steam group
+ Added cl_resend "1"; and cl_resend_timeout "30";
+ Added some configurable graphics settings to [2.2] and renamed the section
+ Added missing viewbob adjustment convar
+ Added log settings to [3.0]
+ Added m_yaw explanation and helpful common values
+ Added more view model and view bobbing presets
+ Added a nade crosshair
+ Added a work-in-progress lagswitch alias
+ Added other two radial radio wheels to F1 and F2 and last radio menu to period/full stop
+ Added a bunch of privacy and safety options to make the game more stream friendly, more secure, and generally more private.
+ Added volume slider settings to [10.0] (Finishing Up is now [11.0])
+ Added draco.cfg with competitive 5v5 settings and begin.cfg to start a tournament that's using draco.cfg
+ Added grenade trajectory settings
+ Added gamemodes.cfg with a chart of gamemode settings

* Moved a bunch of convars to the new Privacy & Safety section [9.1]
* Moved cl_updaterate, cl_cmdrate, sv_minupdaterate, sv_maxupdaterate, sv_minccmdrate
* Updated in-line documentation comments
* Change engine_no_focus_sleep from 0 to 1 miliseconds
* Changed cl_timeout from 30 to 60 seconds
* Fixed missing semicolon
* Moved viewbobing options to aliases
* Fixed some missing/extra whitespace
* Fixed some missing quotes
* Increased volume
* Fixed null cancelling movement
* Radar is no longer square in the scoreboard
* First letter of a players color is now shown on their color circles (in chat and on the radar)
* Changed crosshair to be white and black and change based on weapon.
* Changed sensitivity to match 25600 DPI to my old 1400 DPI @ 3 sens (and added comment about why and how you can do the conversion)
* Added some missing comments
* Made various adjustments to the HUD (including setting the color in [9.0])
* Updated config.cfg
* Renamed csgo_bigfinfrank -> csgo_fin
* Updated README.md with new launch options
* Updated video.txt settings

- Removed sv_max_allowed_net_graph
- Removed nonfunctional sv_cheats toggle
- Removed changed clanid group ID (for "sad" clan tag)
```


## 4.0.3
```diff
+ Viewmodels are now stored in presets (aliases starting with vmp_ short for ViewModel Presets)

* sv_steamgroup is now automatically cleared at launch
* +defuse and -defuse now use +use instead of +use_or_reload.
* +loudshift and -loudshift have both had their volumes increased by 0.025 (2.5%)
* Fixed missing newlines
* Fixed numbering on [3.3.19] and [3.3.20] being one ahead (they're now [3.3.18] and [3.3.19])
* 7.X bind comments about keys being in different sections now use the section number.

```


## 4.0.2
```diff
+ Added configs created by one of my practice maps to .gitignore
+ Updated terminology to align with Google's respectful code style guide
+ Added more ASCII art chat pictures (happy, harder, bongo)
+ Added clanid (steam group clan tag) cycler. By default it cycles through ~12 clanids sorted by length, then it will cycle back through them in reverse order so it loops well visually. (There are an additional 12 interesting clanids you can play with as well).
!!! You should read the comments underneath 3.3.19.
+ Spray menu and right click now clear decals
+ Added snd_mute_losefocus "0"; so game audio isn't muted while you're tabbed into Discord instead of the game for example.
+ Added aliases/ folder, which list other different lists of cfgs.
+ Added keys/ folder with files to list different parts of your keybinds.
+ Added positions/ folder which has setpos_exact commands to teleport to different places in various different maps.

* Rephrased comments for sv_usercmd_custom_random_seed and mm_dedicated_search_maxping to be more clear
* Added a comment with *MY* ping to the nearest servers to *ME*.
* Fixed several typos, made several grammar clean-ups, and some whitespace fixes
* Fixed exojump alias conflict, it (was previously the same as a built-in command) now has been renamed from exojump to exo.
* Cleaned up the ASCII art with blank braile characters instead of single dots in some places.
* Changed alignment for the NCM aliases
* Renamed cheatstart -> cheaton, cheatend -> cheatoff. working on a reliable way to get these working as well, currently they're still very experimental.

- Removed cl_showpos because Valve blocked it in official servers.
- Removed anger management hotline because it 1. wasn't international B. was more than just anger management C. Could hold up someone who is directly interested in seeking help because an angry russian is calling.
- Removed onlyfans bind (alias is still there but I was accidentally pressing it).
```


## 4.0.1
```diff
* Fix linting issues in README.md
* Update config.cfg

! This commit being signed additionally is to verify that the commit for 4.0.0 (d6a67dfd91e402866789c29a89d6e7b49e0437d2) was made by me.
```


## 4.0.0
```diff
+ Added second nag to read the important box at the top of autoexec
+ Added sv_lan to 1.0 client-side networking
+ Added engine_no_focus_sleep to stop the games tickrate and FPS from dropping while tabbed out (1.1 server-side networking)
+ Added additional 3.3.8 knife aliases (a bunch of additional danger zone items)
+ Added documentation commets to 3.3.10 volume bump while slow walking alias
+ Added null-cancel-movement binds which let you move in the opposite direction immediately by hitting the opposite key intead of stopping (press left key while holding right key will make you start going left while you hold the left key)
+ Added clearinputs alias to clear all +input keys
+ Added an experimental smart sv_cheats state setting aliases
+ Added bind listing aliases
+ Added TF2 parity aliases mapping +inspect to +lookatweapon
+ Added mathematically superior zoom_sensitivity_ratio_mouse to actually match non-zoomed sensitivity for small flicks
+ Added comment about alternate rgb hud version
+ Added LWIN and RWIN keys to 7.5 keyboard row 6
+ Added ping (as in latency) and cast_ray to MOUSE3 in 7.6 mouse binds
+ Added bugreporter_uploadasync "1" to 9.0 small tweaks
+ Added section 9.1 with Tweaks from TF2 mastercomfig
+ Added section 10.2 Reset/refresh states which runs hud_reloadscheme;
+ Added clearinputs.cfg which runs the -command for all of the hold-down keys like +forward etc.
+ Added mp_respawnwavetime to practice.cfg
+ Added .vscode/settings.json with an LF line endings enforcement in it
+ Added knife and danger zone item scripts to items/ folder
+ Added keybind listing scripts to lists/ folder

* Specified text file types in .gitattributes
* Removed .vscode/ from .gitignore
* Changed wording around sv_contact
* Changed sv_contact to a csgo specific one
* Replaced cl_forcepreload with the new sv_forcepreload
* Changed mat_monitorgamma comment to use single quotes
* Changed autoknifeinspect to use +inspect alias instead of +lookatweapon
* Swapped use for use_or_reload in 3.3.6 bomb finder alias
* Fixed missing semicolon on angermanagement alias in 3.3.11 chat aliases
* Fixed missing semicolons to the end of section echoes
* Changed F5 to use screenshot instead of jpeg
* Changed 5 key to call slot4 and clear decals instead of cast_ray
* Changed binds to use ncm (null-cancel-movement) directional binds
* Changed G key to use +inspect instead of +lookatweapon
* Renamed section 9.0 from Polishing up some stuff to Small tweaks
* Fixed missing new line in CHANGELOG.md between 3.0.5 and 3.0.4
* Updated config.cfg
* Fixed missing trailing end of file new line in csgo_bigfinfrank.txt and fixed_controller.360.cfg
* Fixed missing semicolons in gaben.cfg and practice.cfg
* Updated launch options

- Removed settings.gg link from autoexec
- Removed trailing spaces from changelogs 3.0.5 and 3.0.4
- Removed whitespace and emoji from 3.0.3 changelog
- Removed CONTRIBUTING.md and CONTRIBUTORS.md because they're not needed no the non-main GitHub branch
- Removed settings.gg reference and contributing section from README.md
- Removed ISSUE_TEMPLATE/ and PULL_REQUEST_TEMPLATE/ as well as their accompanying .keep files since they aren't need on the non-main GitHub branch
```


## 3.0.5
```diff
* Updated warnings at the top of autoexec.cfg
* Updated ## Contributing wording in README.md
* Renamed primary git branch main -> csgo
! Yes there will be other source games besides CSGO soon, next up is TF2
* Renamed LICENSE -> LICENSE.txt

- Removed refreshrate from the non "me-specific" launch options in README.md
```


## 3.0.4
```diff
+ Added missing semicolons to the end of commands & convars
+ Added missing "double quotes" around certain values

* Re-ordered some lines in autoexec.cfg for better aesthetics
* Changed formatting in fixed_controller.360.cfg substantially
* Changed formatting in practice.cfg to be a bit more consistent
* Updated README Todo List
* Changed previous changelogs to consistently use past-tense
* Adjusted whitespace in autoexec.cfg to vertically align some convar values
```


## 3.0.3
```diff
+ Added qmmconnect.dt to .gitignore
+ Added semicolons to the end of commands & convars
+ Added r_cleardecals; to slot keys

* Fixed a couple markdown problems in README.md (plus some slight wording changes)
* Re-ordered crosshair commands, they're sorted by length again!
* Changed kp_multiply (the asterisk on the numpad) to run exec practice.cfg;

- Removed trailing spaces (spaces at the end of lines) in a couple spots
```


## 3.0.2
```diff
+ Added game_mode 1 and game_type 0 to practice.cfg (this sets the server to competitive)
+ Added launch options (with explanations) to README.md
+ Added 'hotswap' aliases to change preferred tickrate for: 16, 32, 64, 128, 256, and 512 tick
+ Bound cast_ray command to 4
+ Added csgo_bigfinfrank.txt to the GitHub Repo (you no longer need to got Settings.GG to get it!)
+ Added toggle aliases for aliases that previously directly used the "bind" command
! THE ABOVE CHANGE MEANS THAT YOU NEED TO SWAP YOUR lefthand ALIAS TO USE handswap INSTEAD

* Changed 11.0 echo to say "Game info and Gaben" instead of "Info and Gaben"
* Updated TODO list
* Updated some documentation
* Fixed some formatting
* Changed WASD To ESDF (more bindable keys within reach, it's better long term but hard to adjust)

- Commented out bindings in fixed_controller.360.cfg, you should use the ones added to autoexec.cfg in v3.0.1 instead.
- Removed some comments from practice.cfg
```


## 3.0.1
```diff
+ Added practice.cfg, which enables various practice configuration settings
+ Added +loudshift and -loudshift aliases to increase volume while shift-walking
+ Added "Damage Given" at the start of the clearchat alias to clog up people with Damage Given filters' screens
+ Added controller binds for the Xbox One/Xbox 360 (probably also works for ps3/ps4/ps5 and steam) controllers
+ Added scoreneton and scorenetoff aliases that are toggle versions of +scorenet and -scorenet intended for controller

* Replaced togglescores with scoreneton in controler binds
* Updated crosshair (thickness & size 1 -> 0.5), updated crosshair code
* Changed sensitivty from 2 to 3
* Changed all instances of +speed to use the new and improved +loudshift
* Changed "Damage Given" filter to look for the more specific "Damage Given to " (this removes one unnecessary line from being shown and lowers targetted attacks like the clearchat one added in this update)
* Adjusted non-functional formatting (stuff like whitespace and new lines)
* Finished off some more in-line documentation
* Changed sv_contact email **THAT YOU SHOULD HAVE ALREADY CHANGED ANYWAYS**
```


## 3.0.0
```diff
+ Added hostname that credits this project to 0.0
+ Added documentation for every remaining command with an explanation given by Valve
+ Allowed and enabled use of net_graph "2" to display incoming/outcoming data statistics
+ Added r_eyemove "0" which disables eye animations that are hidden from view on most models anyways
+ Added cl_fixedcrosshairgap "-4" and set cl_crosshairgap to -2 (previously -3)
+ Added cl_show_observer_crosshair "2" to 8.0 hud settings

* Made binds capitalised to match Valve-generated config.cfg values
* Made crosshair smaller (crosshair_size "1", used to be 1.5)
* Disabled crosshair transparency
* Updated crosshair code
* Moved Less-important note about VSCodium to CONTRIBUTING.md
* Moved trusted_launch_info below version and status in 11.0
* Changed 1.0 and 1.1 to say client-side networking and server-side networking
* Changed max FPS down to 1000, going too high can cause physical damage to some GPUs, pointlessly wears down your GPU, and wastes power.
* Changed 3.2 shorthand convars to shorthand commands (because there is a difference)
* Replaced convar with commands in some places (a convar stores a value, a command does not)
! The change directly above affected the 2.0.0 and 2.1.0 changelogs, so they have been updated

- Removed Note about mm_dedicated_search_maxping because players are warned in-game if their ping threshold is too low
- Removed -cl_show_team_equipment, cl_cmdrate, net_graph, firstperson, and:
- Removed sv_cheats "0" from 10.0 Finishing Up (sv_cheats is no longer a necessary launch option)
!!! THIS IS A BREAKING CHANGE If you were relying on sv_cheats "0" being called at the end of your autoexec.cfg, add it back.
```


## 2.1.0
```diff
+ Added sv_pure "1" to 0.0 as it's requried to play on any reasonable server including MM
+ Added fixed_controller.360.cfg which is controller.360.cfg with the non-existent convars removed, reducing console clutter
! Please use update to use this CFG for controller support, the old one has been deprecated in the context of this project!**
+ Added third section in category numbers for 3.3.N
+ Added category 11.0 numbering for the end-of-config echos
+ Added version command to 11.0
+ Added note about sv_contact to [IMPORTANT]

* Changed crosshair to be static instead of dynamic (the crosshair code has also been updated)
* Changed 0.0 controller support exec to use fixed_controller.360.cfg (this is in quotes now too, it wasn't before)
* Changed semicolon to directly use the disconnect command instead of the dc alias
* Changed default sv_contact to my email fin@fin.fail (YOU SHOULD CHANGE THIS THOUGH, PLEASE)
* Moved viewmodel_offset_y up one line so they're videmodel_offset_? are ordered x,y,z instead of x,z,y
* Moved commented out rgbhud to the last position in 3.3.N (and updated the comment)
* Fixed typo "Chat can display 8 lines on screen while unfocused" should have been 7 lines

- Removed stopsound and stopsoundscape because they require sv_cheats "1"
- Removed cl_bob_version and cl_bobup because they require sv_cheats "1"
- Removed sv_maxcmdrate (this [doesn't actually exist in CS:GO](https://developer.valvesoftware.com/wiki/List_of_CS:GO_Cvars))
- Removed redundant category comments (ex. "// [0.0] Initialization") because you can see the category in the echo's below
- Removed really old "(0/1)" at the end of 10.0 and 10.1 comments
```


## 2.0.0
```diff
+ Added "ahegao" alias which automatically cycles to the next ahegaoN(0-9) alias
+ Added "butt" alias which cycles through the new buttN(0-9) aliases, posting an ASCII art butt
+ Added "onlyfans" alias which says "no you cannot have my onlyfans" in global chat
+ Added .cfg to all of the exec statements that didn't have them
+ Added status underneath trusted_launch_info in the set of things to echo after Finalization
+ Bound autobuy to F6
!   This is mainly for use in deathmatch where turning off autobuy saves your current random loadout
+ Bound slot11 to -
+ Bound slot12 to =
!   slot12 is the bind for healthshots
+ Documented what each key is inline
+ Added link to the GitHub repo in the loading and loaded credit messages

* Added "doublequotes" to all `echo` for consistent formatting
* Added sv_cheats 0 to noknives alias and added sv_cheats 0 to 10.0 Finalization
!!!   THIS IS A NOTEWORTHY CHANGE, WE NOW AlWAYS ASSUME YOUR SERVER IS RUNNING WITH AND THAT YOU WANT sv_cheats 0   !!!
* Fixed diff formatting for 1.0.15 changelog
* Trimmed ahegao aliases to be 7 lines instead of 10 so that it fits into unfocused chat

- Removed Todo list to from autoexec.cfg in favor of having it in README.md
- Removed sv_cheats 1 in favor of the `+sv_cheats 1` launch option
!!!   THIS IS A BREAKING CHANGE, YOU MUST ADD "+sv_cheats 1" BEFORE +exec autoexec IN YOUR LAUNCH OPTIONS   !!!

! The Todo List has been updated accordingly to follow these changes.
```


## 1.0.15

```diff
+ Added this CHANGELOG.md file.

* Attempted to fix bomb finder
* Updated Todo list
* Moved to use Semantic Versioning

- Removed `cl_righthand 1` from right alt (`ralt`)
!   This was pointless as `x` can be used to toggle `cl_righthand`.
```
