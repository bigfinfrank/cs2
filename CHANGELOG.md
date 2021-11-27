# Fin's TF2 Config Changelog
This file contains the changes made version-by-version from newest at the top to oldest at the bottom.
The TF2 Config started with the my CSGO config 3.0.6 as a base and was edited for TF2 from there, so 0.1.0.
1.0.15 is the first Changelog added and has an incomplete list of changes but the changes still serve as a good example for the diff-like formatting.
New updates are added as a h2 header (`##`) above the previous version (meaning new versions will always be added to the TOP of this document). Changes to the changelog for a previous version are allowed under the condition that they must be documented in a new update (this means there will be a version bump even if no changes are made to any other files)
We use [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) which is the undoubtedly best format for version formatting, please use it for your own projects.


## 0.1.0-rc4
+ Added cl_mute_all_comms "1" to section 0.0
+ Added missing in-line documentation for a handful of convars/commands
+ Added a handful of networking optimisations from various online sources and valve's developer docs
+ Enabled sv_lan "1";
+ Changed engine_no_foucs_sleep time to 1ms which should result in much higher fps and tickrates while tabbed out
+ Set the maximum number of dropped packets to 0 and increased the max uploaded file size to 64mb
+ Added a handful of graphical/performance optimisations to section 2.1
+ Added additional mastercomfig sound settings not included in sound=ultra but in comfig.cfg
+ Added a variety of HUD tweaks including disabling achievements and speeding up animations
+ Added sv_motd_unload_on_dismissal "1"; to free up a tiny amount of RAM
+ Added bugreporter_uploadasync "1"; to alleviate lag spikes when uploading bug reports
+ Added "record fix; stop;" and snd_restart; to reset/refresh states section 9.1
* Fixed some missing semicolons
* Fixed some spaces missing and some extra ones causing comments to be misaligned
* Remove showmapinfo bind and replaced it with a second say_party bind
* Shuffled around some config values to make them more aesthetically pleasing
* Moved hud_reloadscheme to saving section 9.2

- Removed video.txt
- Removed old 3.3.7 knife aliases


## 0.1.0-rc3
+ Added sv_steamblockcheck "4" to avoid playing with any players you have blocked
+ Added description to tf_use_min_viewmodels
+ Added customunbindalljoystick alias that execs customunbindalljoystick.cfg which is also new. customunbindalljoystick.cfg unbinds every joystick (controller) command.
+ Added hud_reloadscheme to section 9.0

* Fixed some inconsistent formatting with newlines between sections
* Replaced cl_join_advertise with tf_party_join_request_mode
* Swapped commented out unbindalljoystick command for the new customunbindalljoystick alias

- Removed +/-defuse alias
- Removed TODO note from cl_observercrosshair
- Removed commented out cl_show_clan_in_death_notice


## 0.1.0-rc2
* Fixed linting problem in README.md
* Added an extra newline before the start of the version h2's


## 0.1.0-rc1
+ Added an end-of-file trailing newline to .gitignore
+ Added a second nag about reading this to the important box
+ Added a custom weapon and camera FOV to section 2.0
+ Added mastercomfig changes ported over by hand, you can support their developers at docs.mastercomfig.com/page/support_me, the included additions are below:
+ Added mastercomfig LOD ultra
+ Added mastercomfig lighting ultra
+ Added mastercomfig ligting ex high
+ Added mastercomfig shadows ultra
+ Added mastercomfig flashlight on
+ Added mastercomfig effects ultra
+ Added mastercomfig water ultra
+ Added mastercomfig particles ultra
+ Added mastercomfig post processing high
+ Added mastercomfig pyrovision high
+ Added mastercomfig romevision on
+ Added mastercomfig motion blur off
+ Added mastercomfig anti aliasing msaa 8x
+ Added mastercomfig texture filter aniso16x
+ Added mastercomfig characters ultra
+ Added mastercomfig decals ultra
+ Added mastercomfig decals models high
+ Added mastercomfig decals art on
+ Added mastercomfig sprays off
+ Added mastercomfig gibs high
+ Added mastercomfig props ultra
+ Added mastercomfig ragdolls high
+ Added mastercomfig 3dsky on
+ Added mastercomfig jigglebones force on
+ Added mastercomfig textures very high
+ Added mastercomfig ropes ultra
+ Added mastercomfig hud player model on
+ Added mastercomfig outlines high
+ Added mastercomfig sound ultra
+ Added mastercomfig flat mouse addon
+ Added mastercomfig no tutorial addon
+ Added mastercomfig null canceling movement
+ Added LWIN and RWIN keys to keyboard row 6 binds
+ Added cl_hud_minmode to use minimal hud
+ Added tf_scoreboard_ping_as_text which changes scoreboard ping to be numbers instead of bars
+ Added hud_fastswitch to avoid having to click an extra time to swap weapons
+ Added semicolons to the end of the lines in gaben.cfg

* Changed tickrate warning to use different verbage and 32 instead of 64 tick
* Changed wording in the sv_contact warning
* Changed sv_contact to tf2cfg@fin.fail
* Changed sv_steamauth_enforce to tf_mm_trusted
* Changed hostname to say TF2 instead of CSGO
* Replaced mm_dedicated_search_maxping with tf_mm_custom_ping accompanied by tf_mm_custom_ping_enabled "1"
* Changed cl_forcepreload to sv_forcepreload
* Changed default tickrate alias from 64tick to 32tick
* Changed net_graphheight to 375 so it fits cleanly on scoreboard
* Replaced CSGO viewmodel customization a TF2 one
* Swapped +lookatweapon for +inspect which is the TF2 equivelant
* Swapped cl_righthand for cl_flipviewmodels which is the TF2 alternative
* Changed crosshair customization to use TF2 equivelant convars where possible
* Replaced game instructor and tip disabling section with the massive mastercomfig section which handles disabling tips in section 5.31
* Updated binds to include TF2 commands and convars
* Updated controller binds to use each "key"s TF2 name
* Changed cl_show_observer_crosshair for cl_observercrosshair
* Replaced hud_showtargetid with tf_hud_target_id_alpha, tf_hud_target_id_disable_floating_health, tf_hud_target_id_offset, and tf_hud_target_id_show_avatars
* Commented out cl_join_advertise and cl_show_clan_in_death_notice so they can be replaced with their probably existent TF2 alternatives
* Commented out unbindalljoystick because it doesn't exist in TF2. This will probably be removed by a custom-made alias that accomplishes the same thing in the future.
* Changed wording at the top of CHANGELOG.md
* Changed wording in CONTRIBUTING.md
* Changed wording in CONTRIBUTORS.md
* Updated fixed_controller.360.cfg substantially so it supports TF2
* Changed practice.cfg to have non-existent/incompatible convars and commands commented out and converted some commands/convars to their TF2 equivelants. This will be redone properly in the future.
* Changed launch options in README.md to reflect the TF2 ones

- Removed sv_usercmd_custom_random_seed because it's a cheat convar in TF2
- Removed svframerate options from the net_graph because they don't exist in TF2
- Removed sv_max_allowed_net_graph and set net_graph to 1 instead of 2 because TF2 doesn't have the same net_graph system as CSGO
- Removed net_graphipc because it doesn't exist in TF2
- Removed view bobbing customization because they're all cheat convars in TF2
- Removed fps_max_menu because it doesn't exist in TF2
- Removed cl_hud_healthammo_style from scorenet aliases in section 3.3.1
- Removed gameinstructor from section 3.3.6
- Removed +/-loudshift aliases because they're basically useless in TF2 as there's no slow-walking and the game overall is much more loud and fast-paced
- Removed the already commented out RGB Hud in section 3.3.13 because the necessary convar cl_hud_color does not exist in TF2
- Removed radar customization which was old section 4.0
- Removed not-in-TF2 convars from the section 4.0 crosshair customization
- Removed various hud convars that don't exist (or apply) to TF2
- Removed cl_use_opens_buy_menu and cl_autowepswitch from section 8.0 because they don't apply to TF2
- Removed cl_disablefreezecam from section 8.0 because it doesn't exist in TF2
- Removed game_type and game_mode becuase they don't exist in TF2
- Removed trusted_launch_info from section 10.0 because TF2 does not support trusted launch.
- Deleted config.cfg because there either isn't or I couldn't find a TF2 equivelant file
- Removed csgo_bigfinfrank.txt because it's going to be extremely incompatible with TF2, a TF2 version might be added in the future but it's unlikely.
