# Fin's CSGO Config Changelog
This file contains the changes made version-by-version from newest at the top to oldest at the bottom.
Updates prior to 1.0.15 have not been (and probably won't be) documented.
1.0.15 is the first Changelog added and has an incomplete list of changes but the changes still serve as a good example for the diff-like formatting.
New updates are added as a h2 header (`##`) above the previous version (meaning new versions will always be added to the TOP of this document). Changes to the changelog for a previous version are allowed under the condition that they must be documented in a new update (this means there will be a version bump even if no changes are made to any other files)
We use [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) which is the undoubtedly best format for version formatting, please use it for your own projects.

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
* Changed semicolon to directly use the disconnect convar instead of the dc alias
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

* Put all `echo` convars in "doublequotes" for consistent formatting
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
