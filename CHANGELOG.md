# Changelog
All notable changes to RusherHack be documented in this changelog.

---

## [v2.0] - January 15th 2024

- Added support for Minecraft versions 1.20.2, 1.20.3, and 1.20.4.
- Added AutoSorter module
  - Automatically sort items in containers
  - Requires Baritone
- Added Chams module
  - Modify the way entities are rendered
- ESP
  - Added Shader mode
  - Fixed CSGO mode not working on storages
  - Improved Box mode
- AutoCrystal
  - Fixed bug causing it to sometimes not place
  - Other improvements/bug fixes
- Search
  - Improved speed of scanning chunks (thanks IceTank)
  - Added Range setting to both Blocks and Entities
- Scaffold
  - Fixed sometimes rubberbanding on 2b2t
  - Added StrictExtend
- NoFall
  - Added Grim mode (works on 2b2t)
- NoSlow
  - Added Webs setting (works on 2b2t)
- Improved SourceRemover
  - Works much better on 2b2t
  - Added Priority setting
- Added MainMenu module
  - Cool looking shaders that get rendered on the main menu.
  - You can modify them in the rusherhack/shaders/mainmenu/ folder
- Added Logo hud element
- Added Background module
  - Particles
  - BouncingLogo
  - Gradient
- Added blur shader
  - HUD module -> Background -> Blur
  - Theme module -> Blur
- ViewModel
  - Added Shader setting
  - Added Shadow setting
- Windows
  - Added icons to each window
  - Added Configs window
  - Added TaskbarSide setting
  - Now scale independently of game gui scale
- Fixed line shader being buggy when far out
- Added Baritone mode to AutoWalk
- Added Baritone mode to AutoTunnel
- Improved rusherhack screen icons
- Improved background rendering of list hud elements
- Added WaypointLocks setting to RotationLock
- Added Abort bind setting to FastBreak Packet mode
- Fixed module profile selection not being saved
- Fixed various bugs in ExtraCraft AutoCraft
- Fixed ExtraSign AutoSign on 2b2t
- Fixed clicking self in Freecam kicking on 2b2t
- Added Bees setting to ExtraTooltips
- Added BlockEntityLimit to NoRender
- Added Glow setting to HoleESP
- Added MacroOutput setting to Hud Notifications
- Plugins/API
  - Added RusherHackAPI#getEventBus
  - Added RusherHackAPI#interactions
  - Fixed plugin .jar files being locked while the game is open
  - Deprecated methods in IPlugin interface
    - Plugin developers should now put metadata in rusherhack-plugin.json
- Many other changes and bug fixes

---

## [v2.0-preview] - December 2nd 2023

- Added Windows
  - Alt manager window
    - Easily switch your Minecraft account
  - Console window
  - Relations window
    - Manage Friends/Enemies
  - Waypoints window
- Module profile system
  - Create different profiles for all module settings
  - Useful for saving configurations for multiple servers
  - Manage via the *config command (window coming soon)
- Added AutoTrader module
  - Automatically trade with villagers
- Added AutoTrap module
  - Automatically traps enemies with obsidian
  - Ported from legacy rusherhack
- Added AntiSpam module
  - Filter spam out of the chat
  - Ported from legacy rusherhack
- Added FastBreak Packet mode
- Added Filter setting to Hud Notifications
- Added Firework setting to MiddleClick module
- Added AutoClose setting to ExtraSign AutoSign
- Added ability to move hud elements on the main menu in the HudEditor
- Formatting of *coords command now uses the Position hud element
- Fixed various bugs and crashes
- [Uploaded javadocs for the rusherhack plugin api](https://rusherhack.org/api-javadocs/)

---

## [v2.0-preview] - October 27th 2023

- Introduced first implementation of the new Plugin system
  - Developers who are interested in creating rusherhack plugins can reference the [example project](https://github.com/RusherDevelopment/example-plugin).
  - The plugin system is currently not enabled by default
    - Add the JVM Argument `-Drusherhack.enablePlugins=true` to enable the plugin system.
    - **DO NOT ENABLE UNLESS YOU KNOW WHAT YOU ARE DOING** or are creating your own plugin.
  - Plugin .jar files can be placed in `.minecraft/rusherhack/plugins/` folder
    - This folder must be created manually
- Improved ElytraFly
  - Control mode with UseFireworks setting now works much better on 2b2t
  - Removed debug message printing
- Added GrimRocket setting to ElytraTweaks
  - Increases the lifespan of firework rockets on 2b2t. Useful for traveling with ElytraFly
- More features from legacy versions have been ported to v2.0
- Fixed various bugs and crashes

---

## [v2.0-preview] - October 7th 2023

- v2.0 is an almost complete overhaul of rusherhack for modern versions of the game.
  - Not all changes are listed.
- Previous versions of rusherhack are referenced to as "legacy" versions.

- This version is still in development, however an early access preview is released.
  - Not all features from legacy rusherhack versions have been implemented yet, but are planned to.


### Added

- Hud
  - Added resizeable hud elements.
    - Can be scaled by dragging the bottom right corner of said hud elements.
  - Added a visual representation for snap points whilst in the Hud Editor.
  - Added snap point at the top-center of the screen.
  - Added visual representation for empty list hud elements whilst in the Hud Editor

- Added Rotations module
  - MoveFix used on 2b2t or other servers with similar anticheats.
- Added Bounce mode to ElytraFly.
  - Works on 2b2t
- Added 2b2t setting to Velocity.
- Added 2b2t setting to NoSlow.
- Added Theme module
  - Control theme-specific settings, such as Color.
  - Will be expanded upon with custom themes.
- Added CustomFont module
  - Allows you to easily control the settings of the custom font renderer.
- Added ElytraTweaks module
  - Quality of life improvements for elytra flying.
- Added MultiTask module
  - Allows you to interact with your hands while eating.
- Added FastUse module
- Added Reach module
- Added Parkour module
  - Jumps when on the edge of blocks.
- Added ArmorSlots setting to XCarry.
- Added command suggestions for command arguments.
- Added screen selector to the right side of all rusherhack screens.
- Added Image mode to ESP.
- Added Control setting to Freecam.
  - Lets you control the player while holding the keybind.
- Added Spectate setting to Freecam.
- Added Sneak setting to Safewalk.
  - 2b2t option.
- Added Riding setting to Safewalk.
- Added AutoJump setting to Sprint.
- Added saving/loading system to BreadCrumbs.
- Added git commit hash to watermark for beta testers.
- Added Preserve setting to ExtraChat.
- Added "UwU" mode to FancyChat.
- Added more condition settings to AutoTotem TotemWhen setting.
- Added Extrapolation setting to BowAimbot.
- Added WhileSprinting setting to Criticals.
- Added Whitelist/Blacklist modes to HotbarReplenish.
- Added Sound option to PvpInfo VisualRange setting.
- Added ActivityCheck setting to AntiAFK
  - Checks if you are actively controlling the player before doing an action.
- Added Cache option to ExtraTooltips Maps setting.
  - Saves map images and retrieves them via name. Useful on 2b2t because of the map id obfuscation.
- Added DynamicColor option to ExtraTooltips Shulkers setting.
- Added Books setting to ExtraTooltips.
- Added NBTData setting to ExtraTooltips.
- Added Size setting to ExtraTooltips.
- Added Delay mode to PingSpoof.
- Added UntilFull setting to AutoEat.
- Added Timer mode to TickShift.
- Added First Person camera mode to FreeLook.
- Added Whitelist/Blacklist mode to FastPlace.
- Added different modes to NewChunks.
- Added HoldY setting to Scaffold.
- Added Expand setting to Scaffold.

### Changes

- The entire base of rusherhack, including most features have been rewritten and improved compared to legacy rusherhack versions

- UI / Graphics
  - More optimized and performant compared to legacy versions
  - Font renderer vastly improved and more accurate compared to legacy versions.

- ClickGui
  - Remade with a more modern design.
  - Search bar has been replaced with a category bar that can transform into search bar.
  - Color pickers have been revamped.

- Hud
  - Hud element positions are now stored relative to the screen size.

- AutoCrystal
  - Has been completely rewritten from scratch with many improvements and fixes.

- ElytraFly
  - Improved ObstaclePasser.
  - Moved Firework mode to a setting in Control mode.

- Scaffold
  - Improved functionality with 2b2t's new anticheat.

- Bind System
  - Binds are now stored in their own folder, separate from module configs.

- Macro System
  - Macros can now be named and are now configured by the name of the macro, instead of the key.
  - Macros can now have multiple commands added.

- Config System
  - The format for all configs have been changed since legacy versions.
  - Configs now automatically save every 5 minutes.
  - Some module-specific config files have been removed and are now stored as module settings.

######
- Rotation logic has been improved.
- Moved Capes setting from the Hud module into its own module.
- Updated *credits command.
- Improved HotbarReplenish logic.
- AutoReconnect increment/decrement buttons have been replaced by a slider.
- Moved ShulkerHighlight setting from ExtraTooltips module to the ExtraChest module.
- ExtraTooltips EnderChest cache is now saved per-account.
- FastPlace no longer tries to use non-block items.
  - Use FastUse for this functionality

### Fixed

- Ping hud element not working on 2b2t.
- Timestamps module showing AM/PM even with 24hr format.
- Many more bugs were fixed as the result of the rewriting process.

### Removed

- EntityDesync module
- PacketFly module
- ElytraFly2b2t module
  - No longer works on new 2b2t anticheat. Use other ElytraFly modes.
- Dismount command
- AntiDeathScreen module
- EXPFast module
  - Replaced by the new FastUse module

---

[Legacy changelogs](https://github.com/RusherDevelopment/rusherhack-assets/blob/main/legacy-changelog.md) (before version v2.0).
