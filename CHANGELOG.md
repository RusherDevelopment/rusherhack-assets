# Changelog

All notable changes to RusherHack be documented in this changelog.

---

## [v2.0.7] - February 2nd 2026

This update for v2.0.7 will come in 2 parts. This first release is for Minecraft 1.20.1-1.21.4

##### The next part will be for Minecraft 1.21.11 and should release April/May. After which, support for Minecraft versions lower than the latest will be discontinued in order to improve maintainability and to avoid having more situations where RusherHack is far behind the latest Minecraft version

- Added Language module
    - Allows you to change the language of RusherHack's interfaces
    - If you want to help translate RusherHack to a different language, you can do so
      here: https://crowdin.com/project/rusherhack/
        - Major contributors to a specific language can receive an exclusive translator cape with the country's flag
        - JVM argument for viewing bleeding edge translations before approval: -Drusherhack.locale.bleedingEdge=true

- ElytraFly
    - Added Firework mode
        - Replaces old fireworks setting in Control mode
        - Leave Strict setting enabled for 2b2t
    - Rewrote ObstaclePasser
        - Added X and Z align settings
        - Fixed not working if baritone was #paused
        - Made compatible with ElytraTweaks
    - Fixed deadlock with Bounce mode's Delay setting
    - Added AutoWalk setting to Bounce mode
    - Fixed Bounce not working while eating
    - Fixed Control Aim mode

- ClickGUI
    - Added Dimming setting to improve readability
        - Dims unfocused parts of the panel
    - Search Bar will now find item when pressing Enter key
    - Improved Color Picker
    - Fixed unpausing the game in singleplayer
    - Fixed setting tooltips
    - Fixed color picker crashing if paste button is clicked with nothing in clipboard
    - Fixed font overlapping issues with searchbar text with vanilla font

- CustomFont
    - Fonts that don't support the current language are now hidden
    - Now gets automatically disabled on systems with Intel GPU
        - Intel's GPU drivers have an obscure bug that causes a crash with the font renderer

- ExtraCraft
    - Added to 1.21.4
    - Fixed many bugs

- ExtraTooltips
    - Added Positioning setting
        - Allows you to have the items rendered directly inside of the vanilla tooltip
    - Rewrote map caching system
    - ShulkerSummary setting now works in Inventory HUD element
    - Improved handling of nested tooltips
    - Maps Slot setting
        - Added stack counts
        - Fixed maps rendering in slots in container tooltips even when setting is disabled

- Moved ExtraTooltips ChatEmbed setting to ExtraChat ImagePreview

- EntityList HUD element
    - Added Item whitelist/blacklist
    - Fixed duplicate entries when players die and respawn on some servers
    - Improved performance


- Added ChunkPos setting in NewChunks Alerts
- Added AutoReauth setting to Alt Manager
    - Fixes "Invalid session" errors that sometimes happen when you join Minecraft servers

- Configs
    - Config manager now uses atomic operations when saving (if supported)
        - Will reduce chance of config files getting corrupted
    - Added Config module to configure the auto save interval
    - Added persistent module configs which allow you to have the same config for a module across different profiles
        - TODO: ADD COMMAND HERE

    - Fixed Configs window resetting modules in the Client category

- ESP
    - Added Square setting in CSGO mode
    - Added Range setting to Entities
    - Fixed Shader mode trying to highlight some block entities that it shouldn't be
    - Fixed block entities not being highlighted if they are the only thing on screen
    - Fixed Shader mode not working on invisible entities

- Aura
    - Now pauses AutoEat
    - Added HitDelay Mode
    - Improved compatibility with Criticals Delay mode
    - Fixed compatibility with AutoTrap

- Rewrote AutoWither
    - Added AirPlace support
    - Added different place modes

- Loader
    - Updated HWID algorithm
        - Should be more consistent on Linux systems
    - Added rusherhack.forceReleaseBuild JVM argument
        - Allows rusherhack+ users to use the latest stable (normal) build
    - Added new error message when FlatPak environment is detected
    - Added an icon to be visible in launchers and modmenu mod

- Added AutoShear module
    - Replaces *shear command

- Rewrote *breed command
    - Now works on 2b2t

- Added *peek enderchest command

- AutoArmor
    - Added PiglinGold setting
    - Fixed trying to use Curse of Binding armor
    - Fixed trying to use unglideable Elytras
    - Added Elytras setting
    - Fixed desync with high ping on 2b2t

- Added "exit" as alias for *shutdown command

- Rewrote Logo HUD element
    - Added custom image mode

- AutoDisconnect
    - Fixed various crashes
    - Added Proximity Portal setting
    - Added TotemCheck to Lethal Crystal setting
    - Added ability to speecify Y coordinate for the Coordinates setting

- Renamed Notifications module to Notifier
    - Added title support to ServerMessage setting

- Added NoJumpDelay module

- SourceRemover
    - Added AirPlace support

- AirPlace
    - Is now only active while block is being held
    - Fixed not placing in liquids
    - Made compatible with other modules that place blocks

- Added Custom setting to ChatAppend module
- Added Name HUD element

- Console Window
    - Added up/down command history

- AutoWalk
    - Added setting to only walk while in flight

- HUD
    - Fixed bug with HUD Editor panel font rendering
    - Fixed list HUD elements not being resorted after font change
    - Improved performance of list HUD elements
    - Fixed crash when joining server with HUD background blur enabled

- Search
    - Added Items setting
        - Allows you to search for specific item entities
    - Fixed IllegalBedrock false positives in the end
    - Fixed rare game freezing when using Alert setting

- Scaffold
    - Fixed trying to place on non-solid blocks
    - Fixed inaccurate hit vectors on blocks w/ dynamic shapes
    - Disabled instant rotations by default
        - Only works on 2b2t when used with ViaFabric with version set <=1.20.6
    - Improved diagonal placements when instant rotations are disabled
    - Fixed attempting to place blocks without collision
    - Fixed compatibility with NoGlitchBlocks

- AutoSorter
    - Added ChestOpenDelay setting
    - Fixed removing target chests if they are being emptied by hopper
    - Fixed rare crash

- Rotations
    - Fixed not properly applying rotation speed when more than one module is rotating in the same tick
    - Fixed not updating travel pitch

- AutoCrystal
    - Fixed rotating even if player has no ender crystals
    - Fixed autoswitch bugs

- FastBreak
    - Fixed packet mode trying to mine water
    - Improved Grim setting after 2b2t's patch
    - Fixed packet mode continuing to render blocks that it failed to break
    - Fix InstantRebreak rendering in liquids

- ExtraChest
    - Rewrote logic
    - Added Buttons UseConfigs setting
    - Removed buttons from recipe screens

- NoRender
    - Added ActionText setting to UI
    - Added PotionInventory setting to UI

- AutoTool
    - Improved Priority setting
    - Fixed attempting to swap from mainhand even if mainhand tool is good enough
    - Fixed compatibility with Baritone
    - Fixed MinDurability not working on instantly mineable blocks

- AutoTrap
    - Fixed not placing blocks with Rotate is disabled
    - Fixed trying to trap Freecam camera entity

- Nametags
    - Fixed text overlapping with vanilla font
    - Improved color settings
    - Fixed not being able to zoom in on nametags
    - Fixed armor overlapping bug

- Rewrote AutoReply module

- Rewrote ClientSideTime
    - Fixed compatibility with Time HUD element and Announcer
    - Added RealLife setting

- SkinBlink
    - Fixed on 1.21.4
    - Made layers toggleable
    - No longer tries to toggle Cape

- AutoTunnel
    - Fixed being offset when standing on non-full size block
    - Removed built in FastBreak

- Durability HUD element
    - Added Offhand setting
    - Added Percentage setting

- Fixed Translate module
    - Now uses a new API
    - Added ability to connect to a custom LibreTranslate server

- Fixed Queue HUD element
    - Now uses api.2b2t.vc API

- Ignite
    - Added Self option to Targets
    - Now can use fire charges

- LagDetector
    - Now disabled in singleplayer
    - Color is now customizable

- InventoryMove
    - Fixed many bugs
    - Added Windows setting

- Inventory HUD element
    - Fixed alpha color not working

- MiddleClick
    - Added BlockCheck setting to Firework setting
    - Improved inventory actions

- PacketLogger and AntiPacket
    - Added Toggle All button
    - Added search bars

- ViewModel
    - Fixed banners rendering twice
    - Fixed compatibility with FutureClient

- Waypoints
    - Fixed tracer not going to interdimensional coords
    - Fixed bug where waypoints would not render depending on the direction the player is facing

- ExtraTab
    - Fixed OnlyShow removing yourself from tablist
    - Fixed name colors not working on servers with non-vanilla text components

- Command Suggestions
    - Fixed banners block argument not containing wall banners
    - Improve suggestions for color setting values
    - Improve suggestions for enum setting values


- Added Dynamic Camera mode to FreeLook
- Added Tracers Self setting
- Rewrote SafeWalk Sneak Strict setting
- Added ability to modify HUD element and Window settings via command
- Added Both mode to Speed HUD element
- Added Statistics setting to FPS HUD element
- Added Short setting to OnlineTime HUD element

- Llamas are now considered a neutral entity in modules
- Baby Piglins are no longer treated as hostile
- Updated default Window positions
- Phase's Pearl mode will now use ender pearls from the player's inventory
- AutoTotem now works whilst in containers
- Cape textures are now only downloaded when needed.
- Cancel BlockTweaks Abort on item switch
- Added OnlyFriends setting to HitboxIgnore Players
- RotationLock Yaw now uses -180 to 180
- Improved *nuker whitelist command

- Fixed Sprint Rage Strict not working on newer Minecraft versions
- Fixed AutoMount and AutoNametag not working on 2b2t
- Fixed performance issues when using alongside a mod that uses Satin library
- Fixed command parser failing with 2 arguments with same name
- Fixed StringSetting value updating during command suggestion parsing
- Fixed blur shader not working correctly on 1.21.4
- Fixed FullBright NightVision setting
- Fixed crash when launching game with mods that add new blocks
- Fixed Announcer spamming XP messages
- Fixed some modules not working at world height
- Fixed some modules trying to place blocks behind world border
- Fixed crash in AutoWeb
- Fixed dimension checks on servers that sends custom levels
- Fixed AntiQuit Close crash
- Fixed Avoid Portals only working on some conditions
- Fixed Jesus working in spectator mode
- Fixed the Flight removing flight while in spectator mode
- Fixed ExtraChat Mentions highlighting removed friends
- Fixed bugs in AntiSpam module
- Fixed game crashing when loading corrupted mappings
- Fixed numerous other crashes and bugs
- Fixed Time HUD element
- Fixed Trajectories path for thrown items
- Fixed *namemc command not working on some platforms
- Fixed *nuker whitelist command not adding all types of blocks from groups


- API/Plugins
    - Added ability to create custom categories for modules
        - ModuleCategory#getOrRegister
    - Added ListSetting
    - Added ModeSetting
        - Enhanced version of EnumSetting
    - Added SplitView to window api
    - Added ability to popup windows on any screen
    - Added ItemRegistry, BlockRegistry, EntityTypeRegistry
    - Added RusherHackAPI#getFieldRegistry
        - Allows plugins to access some fields of internal rusherhack features
    - Added RusherHackAPI#getConfigManager
    - Added RusherHackAPI#getWaypointManager
    - Added AllowExternalModulesInDefaultCategories setting to ClickGUI
    - Added EventPlayerConnection
    - Added EventTravel
    - ClickGUI now sorts external modules
    - Added preliminary support for accesswideners in core plugins
    - Added internal events
    - Separateed Module.drawn from Module.hidden so now it is possible to *drawn an external module without hiding it
      from ClickGUI
    - Improved EventInputTick
        - Easily control input states of the player
    - Commands
        - Added ability to register custom command argument parsers
        - Added a new and improved method of registering sub commands
        - Entire command api is now included and unobfuscated
        - Fixed bug with Enum argument parser
    - Added ContainerUtils
    - Added ItemUtils
    - Fixed HUD element backgrounds rendering even if IHudElement#shouldDrawBackground is false

---

## [v2.0.6] - February 28th 2025

- Added support for Minecraft 1.21.4, 1.21.3, and 1.21.2

- ClickGUI / Theme
  - Added descriptions of modules and settings
  - Fixed search bar showing hidden features
  - Added display scaling for monitors with high resolution
  - Added Screen setting to Theme Blur
  - Added Scale setting to HUD Notifications


- Added FakeFlying setting to ElytraTweaks
  - Makes the server think you are flying when you have a chestplate equipped instead of an elytra
  - Requires you to have a chestplate equipped and an elytra in your hotbar
  - Does not use durability
  - Works on 2b2t
- AirPlace
  - Added Grim setting
    - Works on 2b2t
  - Made compatible with Scaffold
  - Made compatible with SourceRemover
  - Fixed using fireworks
- ExtraTooltips
  - Added Slot setting to Maps
    - Renders maps inside of container and inventory slots
  - Added Summary setting to Shulkers
    - Shows the most common item inside the shulker box
  - Now only renders after the mouse is moved
    - Improves visibility when just trying to quickly peer at items in a chest
- ExtraChat
  - Added PlayerHeads setting
  - Rewrote Mentions setting
    - Added FriendColor setting
  - Rewrote most of the module
    - Should be more compatible with other mods that modify chat
  - Fixed chat rendering under armor
- Scaffold
  - Improved compatibility with AirPlace when using Expand
  - No longer attempts to place if the player is manually sneaking
  - Updated default settings to work on 2b2t
- AutoSorter
  - Added AutoClose setting
  - Improved algorithm
- Borders module
  - Added Axis setting
  - Added Beacon setting
- FastBreak
  - Improved rotations
  - Improved DoubleBreak setting
  - Added render for InstaRebreak
  - Improved compatibility with Nuker
- ESP Tunnels setting
  - Rewrote tunnel detection algorithm
    - Configurable Strictness setting
  - Added Vertical setting
  - Added QUADS render mode
    - Renders tunnels as continuous 3d boxes
    - This mode is quite resource intensive
  - Improved performance of LINES render mode
- ElytraFly
  - Fixed AutoWalk not working if disabling ElytraFly during ObstaclePasser run
  - Fixed bug in ObstaclePasser AxisAlign
  - Fixed Bounce mode not working while Freecam is enabled
  - Fixed ObstaclePasser desync
- AntiSpam
  - Added Combine setting
  - Fixed Frequency setting blocking all messages
- NoRender
  - Added BeaconBeams setting
  - Added ToastNotifications setting
  - Added MapDecorations setting
  - Included primed TNT in FallingBlocks setting
- PvpInfo module
  - Added IgnoreFriends setting to VisualRange
  - Fixed Pearls setting prediction
- NewChunks module
  - Improved accuracy of Palette mode
  - Fixed Palette mode not working if Lithium mod is installed
- Spammer module
  - Added some placeholders
    - <random_player> - name of a random online player
    - <random_player_friend> - name of a random online friend
    - <random_player_nonfriend> - name of a random online player who isn't on the friends list
    - <random_player_enemy> - name of a random online enemy
- AutoDisconnect
  - Fixed IllegalDisconnect setting
  - Fixed YLevel setting
  - Fixed TotemCheck threshold
- NoFall Legit mode
  - No longer uses blocks with no collision
  - Improved block placements
  - Fixed sometimes not being able to retrieve water



- Rewrote Quiver module
- Added NightVision setting to FullBright
- Added Portal setting to Avoid module
- Added Speed setting to Swing module
- Added Beds setting to AutoMount
- Added Filter setting to BindList hud element
- Added TPSSync setting to EntitySpeed
- Added Enemies setting to Tracers Targets
- Added Rotate setting to Freecam
- Added OnlyPitch setting to FreeLook
- Added DurabilityPriority setting to AutoTool
- Added ActivatedSpawners setting to Search Blocks
- Added SpawnerActivation setting to Borders module
- Added Shadow settings to CustomFont module
- Added PauseWhileEating setting to AutoWalk
- Added OnlySprinting setting to Parkour module
- Added ServerMessages setting to Notifications module

- Optimized memory usage of 2d renderer
- Rewrote BoatFly AntiKick
- Improved *hclip and *vclip commands
- Improved BowSpam module
- Improved AutoFish
- Trajectories module now works with BowAimbot
- Moved RichPresence module to Client category
- Nametags now shows enemy colors
- InventoryCleaner can now clean in some other screens instead of only inventory
- Improved ExtraChest command suggestions
- Improved InventoryCleaner command suggestions


- Fixed Search Alert and Sound settings
- Fixed RotationLock Hard setting not working in all directions
- Fixed Greeter sending duplicate messages on some servers
- Fixed bugs in Phase Pearl mode
- Fixed not being able to bind to WORLD1 and WORLD2 keys
- Fixed bug rendering pinned windows
- Fixed some settings in HUD module duplicating on *reload
- Fixed RequirePickaxe setting in AutoMine
- Fixed AutoEXP
- Fixed support on Windows ARM systems
- Fixed ForcePlace not placing item frames
- Fixed ExtraTab not working with some other mods installed
- Fixed bugs with ExtraCraft AutoCraft
- Fixed Time hud element not showing actual in-game time
- Fixed rendering bugs when using with Iris mod
- Fixed Waypoints sometimes not rendering
- Fixed PacketLogger reading static fields
- Fixed Reverse Step


- Plugins/API
  - Added Core Plugins
    - Plugins that are loaded before the game is started
    - Supports creating custom Mixins
    - Example implementation: https://github.com/RusherDevelopment/example-core-plugin
  - Added text component support to the notification manager
  - Added IRenderer2D#_drawTextureRectangle method
  - Added PlayerMessage class for parsing senders of chat messages
  - Added EventInputTick
  - Added support for sub commands with depth > 2


## [v2.0.5] - July 15th 2024

- Added NewChunks mode Pallete
  - Working on 2b2t and other servers on modern versions of the game
  - Credit to etianl and rfresh
- Fixed Tracers transparency setting not affecting Search tracers
- Fixed various other bugs and crashes

## [v2.0.5] - July 6th 2024

- Added support for Minecraft 1.21 and 1.21.1
- Rewrote FastBreak module
- Rewrote and fixed AntiSpam module
- Added Filter setting to ExtraChest Search
  - Makes it so the Steal/Fill buttons only switch items that are highlighted by your search
- Added TNTMinecarts setting to AutoDisconnect Proximity
- Added ChatOutput setting to PacketLogger
- Fixed compatibility with Entity Texture Features mod
- Fixed various bugs and crashes on the 1.20.6 version
- Fixed RichPresence ImageURL not working
- Fixed Direction hud element yaw not being wrapped (why did no one report this to me)
- Fixed Position hud element showing Nether coordinates in the End dimension
- Fixed FastUse not applying to offhand
- Plugins/API
  - Added chunk processor/scanner

---

## [v2.0.4] - June 3rd 2024

- Added support for Minecraft versions 1.20.5 and 1.20.6
- ElytraFly
  - Added OnGround setting to Packet mode
  - Improved Boost mode Automatic setting
    - Now works on 2b2t
  - Fixed obstacle passer not working on Bounce mode whilst the Packet setting is enabled
- Added GrimDisabler setting to ElytraTweaks
  - Requires firework rockets
- Added AutoNametag module
  - Automatically renames nearby entities using Nametag items
- Improved Tracers
- Added Smooth setting to Zoom
- Fixed AutoDisconnect
- Fixed AntiHunger queueing fall damage
- Fixed EntityList hud element lag
- Fixed ClickGui panel dragging
- Fixed Trajectories line ending too early
- Fixed Scaffold command
- Removed commands that grabbed 2b2t statistics (2b2tlist, firstdeath, playtime, seen)
  - This functionality can be brought back with [a community plugin](https://github.com/rfresh2/2b2t.vc-rusherhack)

---

## [v2.0.3] - April 26th 2024

- Added TridentTweaks module
  - Allows you to use the Trident's Riptide enchantment even outside of water/rain
  - GrimDisabler
    - Makes most movement modules bypass 2b2t's anticheat
- Improved ElytraFly module
  - Added Boost setting to Bounce mode
    - Works on 2b2t
  - HighwayObstaclePasser now works when ElytraFly mode is set to OFF
    - Allows you to use the obstacle passer with other modules like Flight
- Improved Flight module
  - Swapped modes Normal and Creative
  - Added VerticalSpeed setting to mode Normal
  - Improved AntiKick setting
  - Added Acceleration setting
- Improved BoatFly module
  - Improved AntiKick setting
  - Reorganized settings to be more clear
- Rewrote Scaffold module
  - Works much better on 2b2t
  - Fixed desync on high ping
- Rewrote AutoSurround module
- Rewrote HoleFiller module
- Rewrote AutoWeb module
- Rewrote AutoTrap module
- Rewrote AutoEXP module
- Improved AutoCrystal module
  - Should multiplace less
  - Improved default config
  - Added more render options
- Improved AutoTotem module
  - Improved reliability
  - Added AutoBlock setting
  - Fixed a rare crash
- Improved Phase module
  - Added Pearl mode
- Improved InventoryMove
  - Added Grim mode
- Improved Velocity
  - Added New Grim mode
  - Added Jump mode
- Improved Greeter module
  - Added Filter setting
  - Made delay only affect non-clientside messages
- Improved Criticals module
  - Added Delay mode
- Added ability to pin Windows
  - Shows window even when you are not in the Windows gui
- Added AirPlace module
- Improved AutoEat module
- Added IllegalDisconnect setting to AutoReconnect
  - Fixes the bug on 2b2t where sometimes after disconnecting the player would remain in the server for a period of time
- Improved NoSlow module
  - Grim mode now works with items in main-hand
  - Added sneak setting
    - Works on 2b2t
- Improved NoFall module
  - Renamed mode Bucket to Legit and added support for other types of items
- Improved AutoMine Feet mode
- Added Speed mode Entity
  - Increases your speed when colliding with pushable entities
  - Works on 2b2t
- Fixed Search module's IgnoreNaturalChests setting
- Fixed Spammer not working with commands
- Fixed bug where macros would duplicate when config was reloaded
- Fixed *baritone command
- Fixed some rendering bugs in the gui's
- Fixed various other crashes and bugs
- Plugins/API
  - Refactored most of the UI related code
  - Improved the Theme api
    - [Example theme](https://github.com/xyzbtw/rusherGUI)
  - Command processor now supports Enum arguments

---

## [v2.0.2] - March 1st 2024

- Added GhostHand module
  - Allows you to interact with containers through blocks
- ElytraFly
  - Improved Control mode with Fireworks
  - Fixed AxisAlign settings
  - Fixed sometimes not being able to interact with containers after using Bounce mode
  - Fixed ObstaclePasser overshooting
- ElytraTweaks
  - Fixed being kicked after being still for 1 minute
  - Fixed firework not despawning if not flying
- AutoCrystal
  - Added Damage Ratio option to Targeting Priority
  - Adjusted rotations
  - Fixed Anti Weakness sometimes not activating
- AntiPacket
  - Fixed packet names not being remapped
- PacketLogger
  - Added packet settings
  - Added LogToFile setting
- FastBreak
  - Added Return setting
  - Fixed various bugs and crashes
- Aura
  - Added Projectiles target
  - Added ArmorStands target
- CustomFont module
  - Added ability to toggle shadows
  - Added settings to toggle CustomFont in specific rusherhack screens
- ESP
  - Added Barrels to Storages targets
  - Added ItemNames
- Added ArmorStands target in Nametags
- Added "Offline Login" button to Alt Manager window
- Added Advanced setting to Timestamps
  - Allows you to use custom date/time format
- Configs
  - Now saved in a way that should prevent corruption
  - Fixed ExtraChest configs not being saved
  - Fixed HitboxIgnore Blocks config not saving
- Added module toggle color settings to HUD Notifications
- Added AutoWither module
- Added Custom mode to Time hud element Format
- Added Timestamps setting to Console window
- Added OpenAnywhere setting to Theme module
- Added Self setting to ExtraTab colors
- Added ability to MiddleClick Friends through blocks
- Added ability to toggle waypoints via the Waypoints window
- Improved AutoMine Feet mode
- Improved efficiency of HotbarReplenish
- Fixed not being able to reference items in commands
- Fixed AutoTrader not opening level 1 trades
- Fixed Sprint module rubberbanding when holding opposite movement keys
- Fixed bug that would cause hud elements to move after resizing the game window
- Fixed ViewModel Shader not outlining maps
- Fixed AutoReconnect crash
- Fixed various other crashes and bugs
- Plugins/API
  - Added new events
    - EventAddChat
    - EventChatMessage
    - EventScreen
    - EventNotification
  - Added ability to register settings to Windows
  - Fixed plugin modules not being controllable via command
  - Exposed more functions in IRelationManager
  - Refactored logging system
  - Added ability to create graphics from an InputStream

---

## [v2.0.1] - January 21st 2024

- Fixed Shader ESP not working on some systems
- Added AxisAlign setting to ElytraFly ObstaclePasser
- Added OccludeDistance setting to NoRender ItemFrames
- Fixed AutoTrader ignoring first trade
- Fixed compatibility with OptiFabric
- Fixed bugs in AutoCrystal
- Fixed Nuker trying to mine non-solid blocks
- Logs folder no longer gets cluttered with old log files, they get moved to an archive folder
- Fixed various crashes and other bugs

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
