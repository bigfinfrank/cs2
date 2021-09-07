# Fin's CSGO Config Changelog
This file contains the changes made version-by-version from newest at the top to oldest at the bottom.
Updates prior to 1.0.15 have not been (and probably won't be) documented.
1.0.15 is the first Changelog added and has an incomplete list of changes but the changes still serve as a good example for the diff-like formatting.
New updates are added as a h2 header (`##`) above the previous version (meaning new versions will always be added to the TOP of this document). Changes to the changelog for a previous version are allowed under the condition that they must be documented in a new update (this means there will be a version bump even if no changes are made to any other files)
We use [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) which is the undoubtedly best format for version formatting, please use it for your own projects.



## 3.0.3
```diff
+ Added qmmconnect.dt to .gitignore
+ Added semicolons to the end of commands & convars
+ Added r_cleardecals; to slot keys

* Fixed a couple markdown problems in README.md (plus some slight wording changes)
* Re-ordered crosshair commands, they're sorted by length again! 😄
* Change kp_multiply (the asterisk on the numpad) to run exec practice.cfg;

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
* Fix some formatting
* Change WASD To ESDF (more bindable keys within reach, it's better long term but hard to adjust)

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
* Changes sensitivty from 2 to 3
* Changed all instances of +speed to use the new and improved +loudshift
* Changed "Damage Given" filter to look for the more specific "Damage Given to " (this removes one unnecessary line from being shown and lowers targetted attacks like the clearchat one added in this update)
* Adjust non-functional formatting (stuff like whitespace and new lines)
* Finish off some more in-line documentation
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

* Put all `echo` commands in "doublequotes" for consistent formatting
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
