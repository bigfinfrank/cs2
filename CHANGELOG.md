# Fin's Garry's Mod Config Changelog

This file contains the changes made version-by-version from newest at the top to oldest at the bottom.
Updates prior to 1.0.15 have not been (and probably won't be) documented.
1.0.15 is the first Changelog added and has an incomplete list of changes but the changes still serve as a good example for the diff-like formatting.
New updates are added as a h2 header (`##`) above the previous version (meaning new versions will always be added to the TOP of this document). Changes to the changelog for a previous version are allowed under the condition that they must be documented in a new update (this means there will be a version bump even if no changes are made to any other files)
We use [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) which is the undoubtedly best format for version formatting, please use it for your own projects.


## 1.0.0

```diff
+ Added cl_forcepreload to client-side networking
+ Added cl_showpos to fin_scorenet
+ Added adjustments to mem_*_heapsize's upper and lower limits
+ Added peer-to-peer limiting convars to Privacy & Safety settings
+ Added check to prevent players blocked through Steam from joining the server.

* Updated .gitignore with
* Updated sv_contact from csgocfg to gmodcfg (you should still change this please)
* Moved sv_forcepreload to server-side networking
* Updated various echos and comments.
* Updated Hold-for-melee alias to be use weapon_crowbar instead of slot3.
* Updated fin_loudshift to fin_loudwalk to match gmod's speed versus walk functionality.
* Lowered lag swith rate and commented-out fps_max values to their gmod minimums
* Simplified and improved fin_fpsbugfix
* Updated binds, merging my CSGO and default gmod binds together.
* Enabled sv_consistency
* Updated volume sliders section
* Updated snd_mixahead to severely break audio (see comment)

- Removed numerous convars, cfgs, aliases, and concommands that aren't present in gmod.
```
