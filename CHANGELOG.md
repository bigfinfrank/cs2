# Fin's CSGO Config Changelog
This file contains the changes made version-by-version from newest at the top to oldest at the bottom.
Updates prior to 1.0.15 have not been (and probably won't be) documented.
1.0.15 is the first Changelog added and has an incomplete list of changes but the changes still serve as a good example for the diff-like formatting.
New updates are added as a h2 header (`##`) above the previous version (meaning new versions will always be added to the TOP of this document). Changes to the changelog for a previous version are allowed under the condition that they must be documented in a new update (this means there will be a version bump even if no changes are made to any other files)
We use [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) which is the undoubtedly best format for version formatting, please use it for your own projects.


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
