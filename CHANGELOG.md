# Fin's CS2 Config Changelog
This file contains the changes made version-by-version from newest at the top to oldest at the bottom.
Updates prior to 1.0.15 have not been (and probably won't be) documented.
1.0.15 is the first Changelog added and has an incomplete list of changes but the changes still serve as a good example for the diff-like formatting.
New updates are added as a h2 header (`##`) above the previous version (meaning new versions will always be added to the TOP of this document). Changes to the changelog for a previous version are allowed under the condition that they must be documented in a new update (this means there will be a version bump even if no changes are made to any other files)
We use [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) which is the undoubtedly best format for version formatting, please use it for your own projects.


## 5.0.0-beta10
```diff
+ Added fin_echo to allow quick changes between the echo and echoln concommands.
+ Added aliases_desubtick.cfg to ./config/aliases/ with desubtick aliases (no more exec console spam!)
+ Added defensive-value-fetchers to ./config/defensive_values/ which allows you to dump the current values of (most) defensive convars to console. (use fin_def_fetch)

* Fixed fin_scoreboardfix being missing before tab has been pressed
* Fixed stray = sign causing an unknown command error in console
* Uncommented fps-based lag switch and renamed it to +/-fin_lagswitch_fps

- Removed nav_clear_attribute from debug.cfg because it required an argument and didn't really fit into debug.cfg
```


## 5.0.0-beta9
```diff
+ Added close_buymenu after buymenu bind to remove the blur and post processing filters from behind the buy menu screen
+ Added cl_show_equipped_character_for_player_avatars true
+ Added enable_priority_boost to visuals.cfg
+ Added input_button_code_is_scan_code to binds.cfg
+ Added sv_disable_observer_interpolation true to safety.cfg and practice.cfg

* Fixed some incorrect exec paths after beta8's folder restructure
* Reordered some convars
* Adjusted whitespace
* Uncommented snd_mix_async because it's only developmentonly and not actually removed
* Replaced commented-out cl_freezecameffects_showholiday 0 with sv_holiday_mode 0, which indirectly accomplishes the same thing.

- Removed dm_reset_spawns and reload_store_config from debug.cfg because they were causing crashes
- Removed volume from audio.cfg in favor of using -fin_loudshift to set it.
```


## 5.0.0-beta8
```diff
+ Added fin_scoreboardfix and fin_scoreboard_off to fin_controls.cfg to fix the issue where you can't bring up the scoreboard at the end of matches
+ Added sv_merge_changes_after_tick_with_calcdelta 2, fs_report_sync_opens 1,  and cl_error_report_time 10 for extra debug info in console
+ Added sv_pure_trace 1 to practice.cfg and safety.cfg
+ Added snd_steamaudio_enable_perspective_correction true to audio.cfg

* Updated launch options, they're now actually fully finalised with documentation.
* Updated README
* Moved boot.cfg out of ./cfg/ and into the root of the project next to autoexec.cfg
* Moved desubtick and rainbow_crosshair folders from ./cfg/aliases/ up to ./cfg/
* Renamed cfg folder to config

- Removed fix_mouse2 and unfix_mouse2
```


## 5.0.0-beta7
```diff
+ Added cl_drawhud_force_deathnotices, cl_drawhud_force_radar, hidehud, spec_hide_players, hud_showtargetid, cl_drawhud_specvote, to ui.cfg and skinpictures.cfg
+ Added r_dof_override false and r_player_visibility_mode 1 to visuals.cfg
+ Added cl_server_graphic1_enable and cl_server_graphic2_enable
+ Added cl_new_user_phase -1 to init.cfg
+ Added tv_relayvoice, tv_relayradio, and tv_show_allchat (all false) as well as cl_chatfilters (default all-on) to safety.cfg,
+ Added ignorerad and ignoremsg bound to F7 and F8 respectively
+ Added cl_dm_buyrandomweapons to misc.cfg
+ Added hud_fastswitch 1, cl_inventory_debug_tooltip true, and cl_inventory_saved_filter2/cl_inventory_saved_sort2 to ui.cfg with documentation comments
+ Added "cyclevar fps_max 0 32" as a bind to "Q", allowing for infinite perfect bunnyhops.
+ Added hostname, name, tv_name, and tv_title to debug.cfg
+ Added mouse_inverty, option_duck_method false, option_speed_method false, and cl_scoreboard_mouse_enable_binding +fin_desubtick_attack2 to controls.cfg
+ Added snd_spatialize_lerp (L/R Isolation) to audio.cfg
+ Added mp_logdetail 3, mp_logmoney true, and mp_logdetail_items true to practice.cfg and misc.cfg
+ Added nextmap_print_enabled false to safety.cfg and practice.cfg
+ Added mp_spectators_max 2147483647 to practice.cfg to allow demonstrations for more than 2 players.
+ Added "Clearing and resetting..." sections to debug.cfg to reset/purge/clear/flush/reload all possible things.
+ Added Resetting binds section to the start of binds.cfg to ensure a clean slate.

* Fixed jumped alias to be fin_jumped in a few spots
* Increased sv_unlockedchapters from 1 to 2147483647 (it's max)
* Changed SCROLLLOCK to exec practice.cfg and skinpictures.cfg instead of directly adjusting convars
* Changed KP_MINUS to turn off the experimental screen blocker when reloaded
* Moved some convars from aliases_init.cfg to init.cfg
* Reordered various lines
* Replaced clutch_mode_toggle with toggle cl_clutch_mode in F4 keybind
* Adjusted whitespace and new lines as per usual
* Changed dbg alias to clear console prior to dumping information
* Finished launch options section of README
* Updated joystick buttons to use their new native names

- Removed unnecessary crosshair color changes from ./cfg/aliases/rainbow_crosshiar/*.cfg
- Removed commented out reset/refresh states section from loader.cfg
- Removed fixed_controller.360.cfg
- Removed ./cfg/utility/hardcode_fixes/ because we can apparently use cl_scoreboard_mouse_enable_binding with (desubticked) aliases.
```


## 5.0.0-beta6
```diff
+ Added sv_playerradio_use_allowlist to practice.cfg and safety.cfg
+ Added sv_radio_throttle_window to practiec.cfg to disable radio command limits
+ Added jumpbug alias
+ Added rainbow crosshair aliases set to fin_task9 (triggered on mouse movement) in aliases_ui.cfg and ./cfg/aliases/rainbow_crosshair/
+ Added experimental fin_blockscreen alias to aliases_ui.cfg to prevent spectators with cl_show_observer_crosshair 2 (and sometimes 1) from seeing your screen.
+ Added snd_headphone_eq "1" to audio.cfg
+ Added cl_radial_radio_tap_to_ping to ui.cfg
+ Added crosshair true and fin_blockscreen_on beneath crosshair settings in ui.cfg
+ Added safezonex and safezoney both set to 0.9 to visuals.cfg
+ Added panorama_max_fps and panorama_max_overlay_fps to visuals.cfg
+ Added cl_ragdoll_limit -1 to visuals.cfg
+ Added cl_drawhud false, cl_draw_only_deathnotices true, cl_drawhud_force_teamid_overhead -1, crosshair false, and r_show_build_info false to skinpictures.cfg

* Fixed extra newlines in a few places
* Changed practice config server_secrets.cfg location
* Changed practice.cfg bot_quota_mode from match to normal
* Updated launch options with some significant
* Adjusted whitespace and new lines throughout
* Renamed fin_desubtick_jumped back to fin_jumped (accidentally renamed it with a ctrl + h in the project before)
* Properly named null cancel movement aliases
* Reordered various aliases within their same respective files
* Shortened reddit links in credit comments
* Renamed fin_yawpitch and fin_pitchoverride to fin_override_yaw and fin_override_pitch respectively
* Changed the way nade crosshairs size multiplication is handled
* Updated crosshair
* Fixed desubtick aliases again, and added a backup method that only works for actions that don't need to be held.
* Fixed +bugvoice missing the .cfg file extension in ./cfg/aliases/desubticked/
* Fixed missing semicolons after some convars
* Changed r_show_build_info from false to true to see the added debug info
* Changed r_fullscreen_gamma from 1.6 to 2.2

- Removed old files from CSGO, leaked builds, and limited test. (config.cfg, csgo_fin.cfg)
- Removed unused/redundant movement aliases
- Removed fin_clear_lookatweapon from G key (+lookatweapon) to hopefully fix some weird inspect edge cases
- Removed temp.cfg
```


## 5.0.0-beta5
```diff
+ Added fin_vmp_knife and set weapon slot keys to change viewmodel.
+ Added sv_unify_random_seed true to networking.cfg and practice.cfg
+ Added script_reload_code "kz" to practice.cfg to load kz script (https://github.com/bigfinfrank/cs2-kz-lua)
+ Added fix_mouse2.cfg and unfix_mouse2.cfg to ./cfg/utility/hardcode_fixes/ to fix interaction with UI elements that are hardcoded to listen for keys directly bound with +attack2
+ Added +/-bugvoice and +/-quickgearradial to ./cfg/aliases/desubtick/ folder with their own CFGs, aliases_controls.cfg with their shorthand fin_deubsticked_* aliases, and to aliases_init.cfg with their fin_clear_* aliases.
+ Added sv_invites_only_mainmenu (separate from cl_invites_only_mainmenu) to safety.cfg and practice.cfg
+ Added bind for the menu key (APP) to binds.cfg (and updated 60percentrow6.cfg)
+ Added server_secrets.cfg.example and added server_secrets.cfg to .gitignore
+ Added boot.cfg which is intended to be executed via a launch option once, allowing you to execute certaing things on game start, but not on autoexec reload.

* Added (un)fix_mouse2.cfg to scorenet and spray_menu
* Fixed some missing/extra newlines and whitespace
* Fixed fin_gaben
* Fixed a few aliases still using non-desubticked variants of their +/- concommands
* Tweaked some comments
* Removed extra [loader.cfg] in an echoln
* Various updates to README.md

- Removed fin_uninspect in favor of fin_clear_lookatweapon
- Commented out soundinfo concommand in practice.cfg because it was causing crashes when run with -dedicated.
```


## 5.0.0-beta4
```diff
+ Added alternate subtick bypass method since Valve patched the alias one.
+ Added cq_netgraph_problem_show_auto true to networking.cfg
+ Added bind to spin while defusing (this needs to be directly bound to a key, by default this is O)
+ Added a bind to do an instant 180 degree turn (this also needs to be directly bound to a key, by default this is P)
+ Re-added section numbers per-file in {curly braces} after the CFG filenames (and updated practice.cfg's because they were still using the old style)

* Updated remaining +/- commands to use their desubticked versions
* Fixed fin_scoreneton and fin_scorenetoff
* FIxed echoes in practice.cfg
* Fixed clear.cfg's first echoln saying "End of" instead of "Start of"
* Reordered practice.cfg sections slightly
* Renamed fin_vmp* to fin_vmp_*
* Moved standard starting column for fin_keycontainer in binds.cfg from column 73 to 93.
```


## 5.0.0-beta3
```diff
* Shortened a changelog entry from beta2 to pass markdown linting.
* Fixed some more linting issues in README.md
* Fixed newlines
* Renamed ./prog/binds.cfg and ./prog/core.cfg to prog_binds.cfg and prog_core.cfg respectively
* Moved ./prog/ & ./keys/ & ./positions/ into ./cfg/
* Prefixed all remaining echolns echoes with their filename
* Prepended & appended Start of <filename> & End of <filename> echoes to all remaining cfgs
* Moved gaben.cfg into ./cfg/utility/
* Fixed a handful of miscellaneous formatting inconsistencies (missing semicolons at the end of lines, semicolons immediately before closing double quotes, etc)

- Removed tournament.cfg
```


## 5.0.0-beta2
```diff
+ Added status_json, net_status, tv_broadcast_status, tv_status, demo_info, install_dlc_workshoptools_cvar, soundinfo to debug.cfg and practice.cfg
+ Added cl_teamcounter_playercount_instead_of_avatars true to ui.cfg
+ Added ui_steam_overlay_notification_position_horz 80 and _vert 0 to ui.cfg
+ Added voice_always_sample_mic true and voice_threshold 0 to audio.cfg
+ Added cl_debounce_zoom false to controls.cfg
+ Added writekeybindings to the end of loader.cfg

* Standardized newlines and whitespace across cfgs
* Reordered convars within their subcategories. They're now generally sorted by prefix first (ex sv_), then by line length up to the final semicolon amongst other lines with the same prefix.
* Fixed a few instances of missing in-line documentation
* Changed cl_hud_color to 12
* Changed hud_scaling from 0.5 to 0.9 as the game clamps the value to a minimum of 0.9 anyways
* Changed cl_clanid to 42297947 so it matches sv_steamgroup
* Changed csgo_monitorgamma to r_fullscreen_gamma because valve renamed it
* Moved engine_low_latency_sleep_after_client_tick from networking.cfg to visuals.cfg
* Fixed linting error in README.md

- Removed cl_showfps "0" from Finishing up stage so it's state is preserved between config reloads, -fin_scorenet can be used to set it to zero via tab.
- Removed fin_rgbhud from fin_keycontainer
- Removed old section numbers from echolns
- Commented out cl_interp and cl_interp_ratio because they're no longer present.
- Commented out echolns for sections that were fully commented out otherwise.
- Commented out hud_reloadscheme because it was given the defensive flag.
```


## 5.0.0-beta1
```diff
+ Added private.cfg to hold passwords and other sensitive values previously kept in the normal autoexec (hidden by new .gitignore change, please use private.cfg.example as a base for your own configs)
+ Set engine_low_latency_sleep_after_client_tick "true" to help lower frametimes, decrease input latency and improve perceived smoothness (to both ./cfg/ and practice config)
+ Prepended file names to echos in brackets (ex. [file.extension])
+ Added alias for infinite zeus exploit (bound to L by default)
+ Added alias for mid-round refund exploit
+ Added alias for free kevlar exploit
+ Added "desubtick" aliases designed to intercept subtick information
+ Added "Start of <filename>" and "End of <filename>" `echoln`s at the start and end of cfgs
+ Added hostname_in_client_status "false" (to both ./cfg/ and practice config)
+ Added sv_vote_allow_spectators "true, sv_vote_allow_in_warmup "true, and mapgroup "mg_custom" to allow for custom map voting when practice.cfg is used on a server.
+ Added healthshot improvements to practice.cfg

* Updated .gitignore
* SIGNIFICANTLY rearranged contents of autoexec-part1 and part2 to have all non-alias categories separated into descriptive files in ./cfg/primary/*.cfg
* SIGNIFICANTLY rearranged contents of autoexec-part1 and part2 to have all alias-declaring categories separated into descriptive files in ./cfg/aliases/*.cfg
* SIGNIFICANTLY refactored clearinputs.cfg, it now subtractively applies to all known +/- inputs 16 times each to combat the +concommand "stacking" bug(?) in CS2
* Moved and renamed ./aliases/ folder to ./cfg/utility.
* Readjusted execs to utilize new layout
* Replaced instances of default subtick-affected commands with their desubticked variants.
* Changed from MIT to the Unlicense.
* Reimplemented mp_forcerespawnaplayers as respawn_player in practice.cfg
- Removed fin_jumpfix in favor of +/-fin_desubtick_jump (which is functionally identical)
- Removed sv_game_mode_flags from practice config
```


## 5.0.0-alpha9
```diff
+ Added cl_showmem to +fin_scorenet
+ Added +fin_jumpfix to remove randomness from bhopping
+ Added fin_onyaw, fin_onpitch, fin_onmousemove as an enhanced "keycontainer" of sorts
+ Added improvised fin_handswap alias
+ Added fin_highveljump to gain faster acceleration when bhopping
+ Added aliases to get each knife in local matches with sv_cheats
+ Added longjump aliases
+ Added null-cancelling movement aliases
+ Added PRINTSCREEN key to row 1 binds
+ Added auto inspect to C4 key
+ Added MOUSE_X and MOUSE_Y to mouse binds
+ Added r_show_build_info "false" and cl_allow_animated_avatars "false" to hud adjustments
+ Added mp_footsteps_serverside "true" and sv_server_verify_blood_on_player "true" to privacy & safety
+ Added sv_ignoregrenaderadio "true" to misc sound settings. This can override the server default if run again after connecting to a server, letting you disable "Fire in the hole" on Valve official servers.s
+ Added r_dof_override_near_blurry "80" to finishing up category to make skin inspection dof a single-convar toggle.
+ Added demo_info, trusted_launch status, and sys_info to end of config debug info dump
+ Added some temporary notes about launch options to README.md

* Updated various documentaiton
* Disabling physics sleep
* Disabled server hibernation
* Re-enabled developer 1
* Adjusted whitespace & newlines
* Replaced all instances of +jump with the improved +fin_jumpfix
* Adjusted SCROLLOCK skin previewing bind
* Improved clear.cfg to involve the minimal amount of spam.
* Changed cl_color to green (1)
* Adjusted autoexec.cfg loader to be single-lined
* SIGNIFICANTLY refactored practice.cfg, merging changes from the CSGO draco server.cfg as well.

- Removed some convars from skinpictures
- Removed items folder and it's contents
```


## 5.0.0-alpha8
```diff
+ Added master volume setting

* Fixed linting issues in FUNDING.yml, super-linter.yml, and README.md
* Decreased mm_dedicated_search_maxping from 65 -> 25
* Changed streamer mode privacy settings to false by default as they're broken currently.
* Updated volume sliders

- Commented out fin_128tick as it's broken currently.
- Removed fin_nextxhair from fin_keycontainer as it was distracting with the more vivid colors
```


## 5.0.0-alpha7

```diff
+ Explciitly marked text file extension formats as text in .gitattributes
+ Added cs2 default configs to .gitignore
+ Added cq_netgraph to fin_scorenet
+ Added fin_uninspect workaround alias to fix knife inpsection (going to trial this concept on other binds)
+ Added fin_thermalpaste chat aliases
+ Added auto inspect functionality to nade crosshair
+ Added timescale adjusetment binds to [, ], \
+ Added cl_silencer_mode "0" to small tweaks
+ Added randomised passwords to Privacy & Safety settings
+ Added volume percentage cheat sheet under "Sliding volume sliders"

* Rewrote README.md
* Commented out clear cfg execution in autoexec-part1.cfg
* Updated in-line documentation
* Updated mat_monitorgamma -> csgo_monitorgamma
* Adjusted whitespace
* Fixed loudshift volume values to match CSGO by percentage
* Changed crosshair
* Removed .00 from the end of a few whole integers
* Updated quit_prompt bind to use the new cs_quit_prompt
* Updated comments

- Removed/replaced/commented out instances of rc and clear decals as they currently don't exist.
```


## 4.2.1

```diff
+ Added cl_connection_trouble_show "1"; to indicate network instability in the top right while playing
+ Added net_steamcnx_enabled "2"; to force use of steam networking to avoid IP leaks
+ Added griefing buy bind to purchase an R8 and "fun" utility.
+ Added fin_streamermode toggle
+ Added fin_toggleinspect alias for take screenshots of skins.
+ Added the three in game screenshot concommands to the F12 key which also takes a steam screenshot
+ Added viewmodel adjustment binds to PGUP/PGDN and numpad number keys 1 through 9
+ Added sv_prime_accounts_only "1" to Privacy & Safety settings.
+ Added server.cfg based off of the old draco.cfg, designed for a private skin inspection server.
+ Added more formatting settings to .vscode/settings.json
+ Added extensions.json with a CFG syntax highlighting recommended extension.

* Changed cl_clanid
* Lowered mm_dedicated_search_maxping from 135 to 65.
* Adjusted whitespace
* Increased loudshift volume by 0.15 (0.15 -> 0.3 and 0.1 -> 0.25)
* Fixed chat aliases to use fin_ prefix
* Fixed fin_vmphighfov to use Y offset depth of 2 instead of -2.
* Changed MOUSE5 to use the griefing buy bind instead of the AWP.
* Changed video.txt from exclusive fullscreen to borderless windowed.
* Adjusted CHANGELOG.md for better Markdown compliance.

- Removed fin_clanid from fin_keycontainer.
- Removed autoknifeinspect from "4" key, replaced with normal slot3 concommand.
- Removed old tournament-style Draco server config.
```


## 5.0.0-alpha6

```diff
+ Added alias cfg for taking high quality pictures of skins
* Replaced remaining echo's with echoln
```


## 5.0.0-alpha5

```diff
* Fixed whitespace alignments
* Updated inline documentation
* Moved cl_hud_color comments to [8.0]
* Updated boolean convars to use true/false in practice.cfg and fixed_controller.360.cfg
* Changed practice.cfg bot_kick and bot_stop to "all" to be more explicit
* Changed practice.cfg mp_items_prohibited to "" instead of "0" since it's a list
* Renamed draco.cfg to tournament.cfg
* Commented out CS2-removed convars from tournament.cfg
* Updated gaben.cfg to use echoln instead of echo

- Removed old apply_crosshair_code comment
```


## 5.0.0-alpha4

```diff
+ Rainbow crosshair is now synced with rgbhud (linear rgb version is commented out)

* Fixed cl_interp_ratio being true instead of 1
* Lower cl_resend from 1 to 0.5
* Updated sv_minrate/sv_maxrate settings to 1000000 (new max)
* Disabled sv_lan
* Changed to 128 tick settings
* Disabled battery saver and changed on-battery settings to the least restrictive
* Explicitly set cl_itemimages_dynamically_generated to render item images dynamically when possible
* Fixed sv_logfile being set to a filename instead of true
* Set sv_log_onefile to true
* Moved more CS2-removed commands to comments
* Updated chat line count comment in 3.3.11 title
* Fixed chat ASCII art alises to use fin_ prefix
* Optimized fin_clearchat for CS2
* Updated RGB Hud to use a better color flow
* Added comments with cl_hud_color numbers, their colors, and their hex & rgb codes.
* Fixed addition and removal of nade crosshair in several binds

- Removed broken and obsolete fpsbugfix alias and cfgs
- Removed jump throw bind
- Removed buyammo2 bind
- Removed broken toggle crouch/sprint
- Removed ping; command from MOUSE3 (latency in console ping command, not player_ping;)
```


## 5.0.0-alpha3

```diff
+ Added clear.cfg as a functional alternative to the (seemingly broken) clear; concmd

* Rename autoexecX.cfg to autoexec-partX.cfg
* Commented out several convars removed in CS2
* Replace all echos with echoln (fixes fin_echo ""; empty newlines)
* Updated rate comments with up to date information around CS2 rate settings
* Updated rate to new maximum (from 786432 to 1000000)
* Updated Lag switch to use new rate minimum and maximum.
* FIxed accidental "a" at the end of 5.0.0-alpha2 changelog
* Boolean convars using 1/0 have been migrated to true/false
```


## 5.0.0-alpha2

```diff
* Changed lines commented out for CS2 reasons to start with // CS2
* Commented out sv_contact
* Replaced all instances of r_cleardecals with cl_decal_clear_world
* Replaced all instances of +/-speed with +/-sprint
* A few whitespace adjustments
* Replaced sv_grenade_trajectory with sv_grenade_trajectory_prac_pipreview in practice.cfg
* Replaced sv_grenade_trajectory_time with sv_grenade_trajectory_prac_trailtime
```


## 5.0.0-alpha1

```diff
! Not released, completely broken.
* Split Autoexec into two halves so that it can be executed fully
* Removed preemptive clear; of console to prevent console bugs
```


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
