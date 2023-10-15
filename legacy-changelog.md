# Changelog
This changelog documents the changes from rusherhack v1.0 to v1.3.2. For changelogs from v2.0 onwards, please refer to [this page](https://github.com/RusherDevelopment/rusherhack-assets/blob/main/CHANGELOG.md)

---

## [v1.3.2] - August 25th 2023

- This is the last update for Minecraft 1.12.2

### Added

- added RestartDelay setting to ElytraFly2b2tNew
- added Distance setting to ElytraFly2b2tNew ObstaclePasser
- added Delay setting to AutoTool
- added Item sort mode to AutoSorter
- added FillInventory setting to AutoSorter
- added Hoppers setting to ExtraChest Containers
- added PauseBaritone setting to SourceRemover
- added Strict setting to Scaffold Tower setting
- added Slabs setting to Safewalk
- added WallRange setting to SourceRemover
- added Off mode to AutoSorter Selection setting
- added Durability setting to AutoTool
- added Sway setting to ViewModel
- added ItemFrames setting to NoRender Entities
- added Differenciate mode to the interdimensional setting in the Position hud element
- added ability to search for specific recipes in *recipe list command
- added Constant Rotate mode to Scaffold
- added Info setting to Notifications InGame setting
- added ability to toggle specific waypoints
- added Others setting to DeathFilter DeathSound
- added Waypoints window
- added Frequency setting to Colors Rainbow Settings
- added Filter setting to Greeter
- added Coordinates setting to AutoDisconnect Proximity; you can set coordinates using *autodisconnect coordinates <x> <z>
- added Fill mode to NewChunks
- added "MacroOutput" setting to Hud Notifications
- added StripBlankLines setting to ExtraChat
- added ShiftClick setting to XCarry
- added ability to specify items by name in ExtraChest

### Changes

- rewrote SourceRemover module, much more consistent
- switched to device-code flow for microsoft account authentication in the account manager
- improved AutoArmor; it should no longer close elytras
- rewrote AutoTool logic
- changed Greeter clientside chat color to light gray
- Hud Similar Filter now filters notifications from visual range
- replaced Private setting in Greeter with ClientSide setting with option to change where they are displayed
- improved RotationLock Hard setting

### Fixed

- fixed mobowner
- fixed Hud modulecommandoutput bug
- fixed vanilla lag from loading a large amount of unicode characters
- fixed Nuker not being able to break crops/flowers
- fixed crash that could happen in Saturation hud element
- fixed bug in potion effect hud element positioning; same thing as issue #1341
- fixed bug with antihunger
- fixed bug in AntiQuit module
- fixed bug in *openfolder command
- fixed HotbarReplenish attempting to refill items with a different name
- fixed AutoTunnel Baritone mode stopping after 100 blocks
- fixed Search bug
- fixed autosorter content mode
- fixed AutoMount trying to mount non-empty minecarts
- fixed crash in AutoSorter
- fixed Crosshair bug
- fixed Velocity not canceling fishing rod pull
- fixed Scaffold desync issue on 2b2t that could happen on high ping
- fixed Step trying to step up blocks it shouldn't when Avoid is enabled
- fixed Safewalk compatibility with Speed module
- fixed deadlocks that made the game freeze while loading
- fixed crash from discord rich presence on some computers

---

## [v1.3.1] - August 16th 2022

### Added

- ElytraFly2b2tNew module
- Added command syntax preview in chat
- Scale setting to Hud module
- Aliases to modules
- Hud notification customization
- Ability to change between specific module modes via command
- World setting to Environment module
- BackgroundColor setting to ClickGui
- Rounded setting to ClickGui module
- Mode setting to Colors Rainbow with Gradient option
- Rainbow/Gradient color overrides for color settings with rainbow option
- Ability to pin windows
- Ability to delete items in item windows with the DELETE key
- Added Buttons setting to ExtraChest
- AutoDisconnect setting to Waypoints
- ModuleCommandOutput setting to Hud Notifications
- TimeLimit setting to Blink
- Strict setting to Step Reverse
- Opacity setting to LogoutSpots Ghost
- FocusedCheck setting to Notifications module
- Acceleration setting to ElytraFly
- BoatFixYaw setting to EntityControl
- Inventory setting to AutoCraft
- "fd3fireworks" recipe to ExtraCraft AutoCraft, for flight duration 3 fireworks
- Distance scaling to LogoutSpots Name render
- PrivateMessages setting to Translate module
- Color setting to Inventory hud element
- Center Speed setting to Anchor
- Center Range setting to Anchor
- Descend Speed setting to Anchor
- Doubles setting to Anchor
- Center RayTrace setting to Anchor
- PotionEffects setting to NoRender Particles
- LineWidth seting to LogoutSpots Render Box
- Trails setting to Trajectories AirBorne
- ElytraCheck setting to AntiHunger
- Layers setting to Chams
- Friends setting to Tracers Players
- Hand setting to Chams
- Information to the progress bar on forge loading screen
- Label settings to Direction and Position hud elements
- Strict setting to ExtraSign
- *seen command (uses LolRiTTeRBot API)
- *playtime command to check how much time a player has played on 2b2t
- *firstdeath command (uses LolRiTTeRBot API)
- History scrolling to Console window text field
- Others setting to ChorusControl
- ClickType setting to Nuker
- Targeting setting to Nuker
- Containers setting group to ExtraChest, for toggling which containers it will work in
- Duration setting to Hud Notifications
- 1 second rate limit to Search Blocks alerts

### Changes

- HWID algorithm for mac devices updated again. Mac users will need to request a hwid reset
- Rewrote Translate module
- Made HUD module toggleable
- Default ClickGui color
- Packets window is now sorted alphabetically
- Game timer speed now has a minimum of 0.01, you can disable this by setting "-Drusherhack.mintimerspeed=false" in startup arguments
- *yaw command can now rotate you towards a waypoint by specifying the waypoint name
- The toggle message for toggling hud elements via command now checks for the ModuleToggle setting
- Improved Avoid Unloaded setting
- Refactored Rainbow settings in Colors module
- Made Trajectories predictions toggleable
- Refactored Baritone module settings, made the setting overrides toggleable
- Rewrote XQZ Chams mode
- Improved Step consistency when stepping up 2 blocks
- Improved 2d nametags positioning
- ElytraFly Vertial Aim mode can now go upwards when holding the jump button
- Spammer Whisper setting now uses /msg instead of /w
- ExtraSign AutoSign setting now saves text that you change while in the sign gui
- Censored alt manager password text fields
- Capes are now based on UUID instead of username
- Improved Nuker Closest priority mode (issue #960)

### Fixed

- ExtraCraft AutoCraft setting
- OnlineTime hud element not resetting time after leaving queue after recent 2b2t queue update
- Scrolling animation in clickgui being tied to framerate
- Bug in *openfolder command
- Bug with colorpicker rgb sliders
- Bug with colorpicker hex field
- Bugs with LogoutSpots
- Step applying timer speed when stepping up slabs
- Main menu crash that happened when using some mods
- RichPresence queue related settings being broken after 2b2t's recent queue update
- Bug in BossStack
- NoRender Particles Explosions setting not working with some other mods
- FullBright Potion mode running out of time
- Bug with PotionEffects hud element
- TimeStamps 24hour time not being calculated correctly
- NewChunks Inverse setting being buggy
- Chams Wireframe bleeding through playermodel even with the depth setting enabled
- Chams Glint setting rendering incorrectly on players
- Layering issues with chams
- ExtraChat MentionSound crash
- Layers setting to Chams Wireframe
- Height setting to Step Reverse
- Typing in hud manager slider settings not working
- Background setting to Hud module with Color setting
- Always setting to InventoryMove Look
- Text in HitboxIgnore command
- NoRender NoCluster setting not being effective while an entity is being damaged
- Spammer reading empty lines in the spammer file
- *2b2tlist command (now uses LolRiTTeRBot API)
- List hud elements aligned to the right not adjusting position when width changes
- Rendering issues with TabGui animation

### Removed

- Legacy Mojang auth from the alt manager
- AutoReconnect Queue setting
- *language command as it is no longer necessary
- Fucker module
- *bedspawn command

---

## [v1.3] - July 4th 2022

### Added

- ChorusControl module
- TickShift module
- Background module
- TrueDurability module
- AntiQuit module
- AutoSorter module
- AntiSpam module
- AutoTrader module
- Logo hud element
- 2b2tQueue hud element
- Weather hud element
- *nuker block command
- *disconnect command
- Horizontal mode in BowSpam BowBomb
- Delay setting in AutoRespawn
- YLevel, Time, and StopAutoRC settings in AutoDisconnect
- Volume setting in Hitmarkers Sound
- Others setting in RangeCircle
- Durability mode in RainbowEnchant
- Damage setting in Notifications
- Smart and SafeRange settings in HoleFiller
- SwitchBob setting in Animations
- Fireworks setting in ForcePlace
- FakePlayers setting in Entities
- Bobbing setting in NoRender Players
- Eating and Criticals settings in NoRender Particles
- Range setting in NoRender NoCluster
- IgnoreHotbar setting in InventoryCleaner
- GlobalColor setting in Hud
- Hide setting in Nametags TotemPops
- ChatEmbed and EnderChests settings in ExtraTooltip
- ItemFrames setting in ExtraTooltip Shulkers
- Dispensers, IgnoreDungeonChests, and ToggleOnDisconnect settings in BaseFinder
- SelfRunOut setting in PvpInfo Potions
- SilkTouch setting in AutoTool
- Throw and SilentThrow settings in EXPFast
- Custom mode in RichPresence
- Mode setting in HoleESP Glow
- Copy mode in ExtraScreenshot
- Width setting in Search DrawBox Outline
- GlintSpeed setting in RainbowEnchant
- Off mode and Search setting in ExtraChest
- Blocks setting in HitboxIgnore
- Animations setting in ExtraChat
- Metadata setting in FeatureList
- Icons setting in PotionEffects
- Shulkers setting in DubCounter
- Interdimensional and Simple settings in Position
- HotbarLock setting in Armor hud element
- ShowHidden setting in BindList
- CombineDuplicates setting in EntityList
- ShowHidden, Enabled, and Disabled settings in BindList
- Label setting in text hud elements
- Color, Animations, and SortMode settings in List hud elements
- shulkerbox wildcard to *search blocks command
- the ability to delete FakePlayers with the *fakeplayer command
- the ability to open other folders in the .minecraft directory from the *openfolder command
- Hide Text and Toggle All buttons in Packets window
- timestamps in Console window
- buttons to modify AutoReconnect delay on the disconnected screen
- the ability to select a specific mode value by middle clicking the mode setting
- the ability to set a precise value in number setting by middle clicking
- hold binds in modules. hold the key while binding for 1 second to toggle
- JVM argument to disable rusherhack baritone integration, "-Drusherhack.disableBaritoneIntegration=true"

### Changes

- Search logic rewritten
- List hud elements rewritten
- NoSlow 2b2t setting updated
- Timer now takes timer priority over other modules
- ElytraFly InstantFly no longer tries to takeoff while in liquid
- sent chat history no longer gets cleared
- MiddleClick Pearl consistency improved
- Waypoints command dimension recognition improved
- ExtraScreenshot now saves images asynchronously
- ExtraScreenshot now copies screenshot links with https protocol instead of http
- AutoSurround Center setting improved
- Step Timer setting improved
- RotationLock Custom settings now allows more precision
- ExtraTooltip settings refactored
- Speed Strafe mode no longer jumps if you are in liquid
- you can now open RusherHack guis on the disconnected screen
- AutoReconnect button placement improved
- HoleESP Double setting improved
- BreakESP self rendering improved
- ESP Tunnels setting is now multithreaded
- damage values can now be specified for ExtraChest items

### Fixed

- AutoArmor being buggy while in containers
- AutoRespawn DeathCoords spam
- AutoDisconnect disconnecting when joining a server to the death screen
- Hitmarkers not being directly in the middle of the screen
- Aura rotate bugs while using WeaponCheck setting
- InventoryCleaner and ExtraChest commands being broken
- rendering issues with NoRender NoCluster
- AutoMount Horses setting not working on skeleton horses
- FullBright bug
- FakePlayers not having invulnerability ticks
- bug when opening Windows module from the ClickGui
- ExtraChat Mentions Highlight formatting bug
- Anchor delay bug
- Friend Manager window not updating
- OnlineTime hud element being affected by Timer module
- LogoutSpots Ghost visual bug
- AutoArmor Durability setting not working with Elytras
- not being able to log into Microsoft accounts in the Alt Manager on older Java versions
- some commands printing "null" into the Console window
- MobOwner bugs
- AutoArmor not equiping armor when a gui is open
- SearchBar bug when typing in slider button
- toggling Speed crashing on the main menu
- Alt Manager crash
- Search Sound crash
- Linux and macOS hwid inconsistencies

### Removed

- AntiBot module
- AutoIgnore module
- Particles module
- Secret main menu shader
- AntiDisconnect setting in AutoReconnect
- Chat setting in AntiAFK

---

## [v1.2.3] - September 5th 2021

### Added

- Anchor module
- InventoryCleaner module
- Environment module
- Entities module
- Quiver module
- CrystalCounter hud element
- DubCounter hud element
- Ability to add items to HotbarReplenish via command and removed item settings
- Offhand setting to HotbarReplenish
- Similar option to Hud Notification Filter setting
- Tunnels setting to ESP
- Glow setting to HoleESP
- Outline Height setting to HoleESP
- Color setting to Chams Glint
- AutoTotem WhileEating setting
- Ghost setting to LogoutSpots
- Containers setting to Regear
- *notify command
- Offhand compatibility to AutoEat
- Offhand compatibility to AutoFish
- PauseBind setting to Baritone module
- Locking setting to ExtraToolips Shulkers
- Extrapolation setting to AutoCrystal Targeting
- Saddles setting to NoRender Entities
- ClientSide setting to NoSwing
- AutoDisable setting to LongJump
- Offhand setting to Swing module
- ChatColor setting to Hud Notifications
- Separate MinDamage and MaxSelfDamage settings to AutoCrystal for breaking with Smart mode
- NoCluster setting to NoRender Entities
- Projectiles setting to NoRender Entities
- Liquid setting to NoRender World
- BeaconBeam setting to NoRender World
- XP setting to NoRender Entities
- Hands setting to NoRender Player
- Durability Threshold setting to AutoArmor
- Option in TPS hud element to show tick-length instead of tick-rate
- Delay setting to AutoMount
- Entities setting to ForcePlace
- Inventory setting to AutoTool
- Endermen setting to Avoid
- Blocks Alert setting to Search
- Blocks Sound setting to Search
- Center setting to SelfBlock
- Mode setting to Time hud element
- HideF1 setting to Tracers
- HorseInfo setting to Nametags
- Settings to Trajectories to toggle different airborne entity types
- Width setting to NewChunks
- Inverse setting to NewChunks
- Burning setting to AutoEat GoldenApples
- *chatappend command
- DepthStriderRequired setting to WaterSpeed
- Separate settings in WaterSpeed for vertical velocity
- WaterRaise setting to Armor hud element
- Fire setting to Fucker

### Changes

- Rewrote Nametags
- Rewrote AutoArmor
- Rewrote AutoTotem logic
- Changed AutoTotem delay setting from seconds to ticks
- Made FastBreak Packet Render render progress
- Made *fakeplayer command copy the player's inventory
- Removed version check in hwid algorithm for Linux devices
- Improved Step
- Improved Jesus Strict while riding entities
- Improved AutoCrystal strict rotations
- Renamed NoSwing module to Swing
- Improved consistency of ElytraFly Firework mode
- Made it possible to toggle debuginfo screen while on death screen
- Made AutoFish automatically cast a hook
- Improved NoSlow Web FastFall
- Made SelfBlock not jump if placing a skull
- Made Criticals not work while in webs
- Made Speed AutoSprint only sprint while moving
- Improved Aura PauseBaritone setting
- Improved AutoWalk PauseOnLag setting whilst using Baritone mode
- Made Blink toggle off after death
- Changed icon for Notifications module
- Changed Speed BPS text from "bp/s" to "b/s"
- Made *travel command travel to waypoint Y level
- Aura is now paused while AutoCrystal is targeting
- Search Entities now ignores the entity you are riding
- Made *waypoints list only list waypoints for the current server
- Made *waypoints del only delete waypoints for current server
- Made Spammer In Order mode start from first message when retoggling module
- Replaced Armor Hud element Percentage setting with Durability setting
- Made AutoTool prioritize hotbar items
- Refactored LogoutSpots settings
- Made Speed mode Ground Strafe not work while sneaking
- Made Speed GroundStrafe mode not work while eating

### Fixed

- Windows 11 compatibility
- AutoCrystal OnlyOwn Break mode not breaking crystals placed from off hand
- AutoCrystal Smart Break mode
- Numerous AutoCrystal bugs
- AutoCrystal WhileEating check not working when eating in offhand
- AutoWalk Baritone mode not being able to walk on diagonals
- AutoEat opening containers
- AutoEat PauseBaritone setting
- AutoSurround placing unnecessary blocks
- Purple chestplate on PlayerView hud element when using Inventory hud element
- AutoCrystal Smart mode not accounting for MaxSelfDamage
- NoFall code running while elytra flying
- AutoEat Return setting
- ESP Light setting not being accurate
- Xray texture bug when using Optifine anti aliasing/shaders
- ESP rendering upside down whilst using Chams Glint
- Notifications Whispers false positive
- ClientSideTime breaking TPS meters
- Bind settings not aligning properly to the right in the ClickGui
- Opening Windows module from ClickGui being buggy
- AutoTotem Health mode not switching back to totem if health was low and AlternateWhen bind was toggled
- SelfBlock not working whilst standing on top of an ender chest
- LogoutSpots rendering spots in other dimensions
- Search not working with skulls
- Speed OnGround Strict setting working while under signs
- AutoMine Feet mode only hitting once even if FastBreak module is disabled
- AutoMine AutoDisable setting
- Chams fill alpha slider not working
- PlayerView hud element not looking at mouse cursor in all guis
- Alignment bug with Direction hud element
- Xray Opacity setting resetting after restarting
- OnlineTime hud element not working after game restart while having the element still enabled
- AutoIgnore Exclusions setting group being empty
- Time hud element 24 hour format not handling midnight correctly
- FastBreak AutoSwitch setting not saving
- Block break lag
- PlayerView hud element following mouse in guis even when Forward is enabled
- Avoid Unloaded priority
- Duplicate tray icons from Notifications module
- InventoryMove "Others" setting working whilst in chat
- PvpInfo StrengthDetect detecting the local player
- Flight Creative mode moving whilst in Freecam
- Speed hud element not saving Average Time setting
- ExtraChat NameProtect setting
- Fucker Lawn breaking grass blocks

### Removed

- ElytraFly2b2t module
- Break Instant setting in AutoCrystal

---

## [v1.2.2] - July 4th 2021

### Added

- Added support for Entities in Search
- Added ColorMode setting to Search
- Added OnlineTime HUD element
- Added Mode setting to Xray
- Added Raytrace setting to SourceRemover
- Added Raytrace setting to HoleFiller
- Added SoftReload setting to Xray and Search
- Added OnGroundStrict setting to Speed (makes OnGround only work while in a tunnel
- Added Raytrace setting to AutoTrap
- Added IgnoreTerrain setting to AutoCrystal Place
- Added CaveFinder mode Wireframe and Thickness setting
- Added Filter setting to Hud Notifications
- Added FullBBItems setting to ESP Entities
- Added OnFire setting to NoRender Entities
- Added HeldItem setting to NoRender Entities
- Added module commands to *help
- Added MiscEntities color setting in Colors module
- Added Strict setting to NoSlow Webs
- Added FastFall setting to NoSlow Webs
- Added YLevel setting to Avoid Void
- Added Doubles setting to HoleFiller
- Added Transparency setting to Tracers
- Added Outline sub setting to Search DrawBox setting
- Added Alert setting to Search Entities setting
- Added Sound setting to Search Entities setting
- Added EntityHit setting to Trajectories Target
- Added CutAway setting to CaveFinder
- Added more customizability to InventoryMove
- Added AutoFocus setting to ClickGui SearchBar
- Added per-item color customizablility to Search (5th argument in the *search command for adding blocks with specific colors)
- Added on ground check to SelfBlock
- Added Average setting to Speed HUD element
- Added group setting compatibility to HUD Manager
- Added Milk setting to AutoEat
- Added ability to reset all module settings "*reset all"
- Added Outline setting to FastBreak PacketRender
- Added AutoSwitch setting to FastBreak Packet mode

### Changes

- Rewrote Chams
- Rewrote PacketFly
- Rewrote AutoEat logic (should fix numerous bugs)
- Improved consistency of SelfBlock
- Rewrote TimeStamps
- AutoTrap now places from back to front
- MainMenu shader is now disabled by default if using integrated graphics
- Improved AntiAFK Baritone algorithm
- Refactored Hud Notifications settings
- Changed default modes for ESP
- Improved AutoCrystal Break Raytracing
- Changed command syntax to allow multiple words per argument with quotes
- Replaced NoRender RidingBoat setting with RidingEntity
- Optimized Airborne Trajectories
- Changed Xray logic and added Opacity setting
- Enabled anti-aliasing for RangeCircle
- Made ClickGui search bar more noticeable
- Search Blocks rendering now uses selection box instead of a full block
- Renamed Timer's "Timer Speed" setting to "Speed"
- Improved FastBreak ready detector
- Refactored FastBreak settings
- PacketLogger now uses MCP names

### Fixed

- Fixed HWID inconsistencies on Linux systems (Requires HWID Reset)
- Fixed NoRender Fog
- Fixed AutoEat sometimes eating multiple golden apples
- Fixed InventoryMove Strict not working whilst sprinting while airborne
- Fixed SelfBlock rubberband rotation
- Fixed Animations AttackBob setting being broken from last update
- Fixed Criticals
- Fixed typo in *xray blocks command
- Fixed AutoWeb appearing to rotate in third person even if rotations are off
- Fixed RichPresence API spam while in queue
- Fixed HorseJump setting in EntityControl
- Fixed EntityDesync crash if toggled on main menu
- Fixed crash with replaymod
- Fixed NoForceRotate Weird mode conflicting with PacketFly
- Fixed PacketFly crashing when disabling on the Main Menu
- Fixed typo in *search blocks command
- Fixed Airborne Trajectories not working for Fireballs
- Fixed Nuker bobbing bug
- Fixed Nuker targeting liquid
- Fixed WaterSpeed going up with space while using Freecam
- Fixed Speed Ground Strafe mode
- Fixed crash when creating module profile with '/' character via window
- Fixed being unable to bind AutoTotem AlternateWhen to MOUSE2
- Fixed InventoryMove Look working while not in a gui
- Fixed Color Picker resetting alpha when changing hue
- Fixed SourceRemover trying to open ender chests
- Fixed HoleFiller sometimes not filling holes near you
- Fixed FeatureList hud element not sorting lower/upper case properly
- Fixed ExtraChest duplicating whitelisted/blacklisted items

### Removed

- Removed FullBright mode Gamma

---

## [v1.2.1] - May 16th 2021

### Added

- Automatic setting to ElytraFly Boost mode (https://www.youtube.com/watch?v=W5R2BAAQbsI)
- FreeLook module
- Baritone mode to AutoWalk
- PauseOnLag setting to AutoWalk
- LogoutSpots setting to AutoTrap
- AlternateBind setting to AutoTotem
- VerticalSpeed setting to ElytraFly
- Glide Speed setting to ElytraFly
- SpeedLimit setting to Boost ElytraFly
- Upwards setting to Boost ElytraFly
- Outline setting to ClickGui SearchBar
- RequiresAutoCrystal setting to AlternateWhen setting in AutoTotem
- Ability to increment enum settings via command
- UseForward setting to ElytraFly Boost mode
- Pause keybind setting to ElytraFly Boost mode
- AutoRedeploy setting to ElytraFly
- Outline options to AutoCrystal Render settings
- Scale setting to Render Damage setting in AutoCrystal
- *namemc command
- InsideCheck setting to SelfBlock
- ReadyColor setting to FastBreak
- PacketRange setting to FastBreak
- Settings to change scale for each axis on ViewModel
- Setting to toggle offsetting while eating on ViewModel
- RequirePickaxe setting to AutoMine Feet mode
- Double and DoubleColor settings to HoleESP
- FallDistance setting to AutoTotem Health mode
- Color settings to customize CSGO ESP HealthBar
- PauseBaritone setting to Aura
- Items setting to Colors module
- AutoDisconnect metadata on FeatureList
- ESP metadata on FeatureList
- Custom Yaw and Pitch settings for RotationLock
- All subsetting to NoRender Skylight setting

### Changes

- Rewrote Installer
- Changed HWID algorithm (if you had a second computer whitelisted you will need to re-whitelist it!)
- Renamed AutoTotem HealthItem setting to AlternateItem
- RotationLock Angles setting is now customizable for both Yaw and Pitch
- Renamed ElytraFly "Strict" setting to "Glide"
- Refactored ElytraFly settings
- Renamed ElytraFly "Spoof" setting to "PitchSpoof"
- Increased ViewClip max Distance to 20
- Refactored ViewModel settings
- Refactored HoleESP settings

### Fixed

- M1 Mac support was fixed by Apple. if you have an M1 Mac make sure you are using the latest update.
- Shader ESP failing to compile on some systems
- AutoTrap targeting freecam entity
- ViewModel FOV not working with Optifine
- FPS lag while using Jesus with particles enabled
- Some crashes when toggling modules from main-menu
- Step settings resetting when launching game
- FastBreak InstantRebreak trying to instantly break bedrock
- NoRender Weather flickering sky bug
- AutoCrystal not targeting people in blocks without bounding boxes
- Notification sound being played at 0,0 in the world
- BaseFinder LlamaThreshold not working
- Friends not saving when removing them via command
- Step Vanilla mode not respecting Upwards setting if disabled
- AutoSurround not toggling immediately when jumping
- Vanilla chunk border rendering while using Freecam
- Chams rendering being buggy when close to a wall
- Bug with AutoEat health mode
- ExtraTab toggle setting rendering below hud elements
- Friends and Enemies not saving after clearing them
- TabGUI gaps from setting groups
- Removing bind from module that is currently bound to a mouse key, to "Mouse0"
- Criticals trying to crit vehicles and other non-living entities
- AutoCrystal appearing to rotate in third person even if Rotate is disabled
- Armor hud element showing negative values when wearing heads
- Compatibility with AutoMine Feet mode and FastBreak Packet mode
- EntitySpeed Strict setting while on snow
- Greeter delay being in milliseconds
- ClickGui SearchBar not being centered when using a gui scale other than 1
- Position hud element sometimes not aligning properly on right side of screen

### Removed

- ElytraFly Constantiam setting
- AutoCrystalOld module
- SmallShield (replaced by ViewModel)

---

## [v1.2] - April 12th 2021

### Added

- Pitch setting to ExpFast
- Totempops setting to PvpInfo
- "Both" option to Hud -> Notifications
- [BARITONE] *travel command to travel to rusherhack waypoints
- Mode setting to Spammer with an option to go In Order
- Whisper setting to Spammer
- Viewmodel module
- Morph setting to RangeCircle
- Strict mode to Jesus
- "Both" option to AutoEat mode
- VerticalMultiplier setting to WaterSpeed
- An AccountManager setting to MainMenu module
- Proper scrolling to the clickgui and hud manager
- Hands setting to ViewModel
- *baritone command
- Color setting to Particles
- CSGOHealthWidth setting to ESP
- Setting groups
- Settings for storages into Colors module
- Line smoothing to Trajectories
- AutoDisable setting to AutoFish
- PanelOutline setting to ClickGui module
- YOffset setting to Nametags
- Shulker cache setting to ExtraTooltip
- AbsorptionCheck setting to AutoTotem Health mode
- *enemy command
- ColoredEnemies setting to ExtraTab
- Delay setting to AutoReply
- Instant mode to SelfBlock
- AutoToggle setting to AutoDisconnect
- Proximity setting to AutoDisconnect and moved Crystal setting to it
- OnlyElytra setting to AutoWalk
- Brightness Table mode to FullBright
- MandelBrot main menu shader
- Random setting to ChatAppend
- RealWorld setting to ClientSideTime
- Visibility settings to Particles
- InstantRebreak setting to FastBreak
- EchestHolding setting to Scaffold
- Boost mode to ElytraFly
- *shear command
- Horses setting to AutoMount
- Inventory setting to HotbarReplenish
- IllegalBedrock setting to Search
- GhostFix setting to BlockTweaks
- PacketRender setting to FastBreak packet mode
- predicate checks for FastBreak's settings
- MaxHeight setting to ExtraTab
- Toggle setting to ExtraTab
- Sorting setting to ExtraTab
- OnlyShow setting group to ExtraTab with Friends and Enemies sub settings
- Ping mode setting to ExtraTab
- A lot of Color settings for ExtraTab
- Light setting to ESP
- HideLiquid setting to CaveFinder
- MD5 mode to FancyChat
- Health setting to LogoutSpots
- Time setting to LogoutSpots
- Vanilla mode to Step
- Baritone compatibility to Sprint
- SpinSpeed setting to AntiAim
- FocusCheck setting to AutoReply
- Hard setting to RotationLock
- 2nd argument for *reset command which allows you to reset a specific setting
- Background setting to NoRender
- ArmorStand setting to NoRender
- BlockBreak setting to NoRender
- ShulkerHighlight setting to ExtraTooltips
- Support for offline accounts in alt manager (leave password empty)
- Support for Microsoft accounts in alt manager
- List argument to *kit command
- Formatting setting to ExtraChat Mention Highlight
- Friends setting to ExtraChat Mentions
- Background setting to ExtraChat Mention Highlight
- Strict setting to EntitySpeed
- Only Skulls setting to SelfBlock
- Only EnderChests setting to SelfBlock
- Shield option to HealthItem setting in AutoTotem
- Exclusions Friends setting to AutoIgnore
- PacketRotate setting to FastBreak
- Rotate setting to SelfBlock
- Cobwebs to Scaffold blacklist
- Circles setting to Particles
- SearchBar to the ClickGui
- *hud command
- Packets window to customize packets for AntiPacket and PacketLogger
- Time setting to PacketLogger
- Range setting to Hud Snapping
- AntiDisconnect setting to AutoReconnect
- Queue setting to RichPresence
- Blocks setting to Scaffold
- *scaffold whitelist and *scaffold blacklist command

### Changes

- Rewrote AutoCrystal
- Rewrote ESP
- Strict Jesus now works better with entities
- Improved speed hud element
- Keybinds no longer toggle while holding F3
- Console output now gets logged to a file
- ClickGui VisiblePredicate is now enabled by default
- Raised fov slider max to 160
- Revamped HitboxIgnore settings
- Search Tracers now use the thickness defined in the Tracers module
- Rewrote color picker and color setting
- LogoutSpots now clear when the module is toggled
- HUD editor manager now uses same scale as clickgui
- HUD editor manager now uses same font as ClickGui
- Changed default settings for AntiAfk
- Improved PotionEffects hud element formatting
- Improved Avoid Void setting
- Separated Llamas from the Donkeys setting in BaseFinder
- Reduced BaseFinder notification spam
- Made AutoExp rotate silently
- Improved strict setting under Criticals
- Replaced Box setting in Trajectories with Target setting with more customizablility
- *clear command now clears chat if typed from chat
- Optifine fast render is now disabled while using ESP to prevent rendering issues
- Improved Scaffold (now works with carpet and slabs)
- Made it so AutoTotem on Health mode switches back to a totem while falling more than 8 blocks
- Maybe fix weird esp optifine crash?
- Clamped TPS Sync in Timer module to prevent freezing
- Improved InventoryMove strict setting
- Nametags for friends now use transparency of the color setting
- Improved PingSpoof
- "/" now gets stripped from config names when creating a new config
- Rewrote binding system; you can now easily bind mouse keys to modules and macros
- Color picker preview no longer displays transparency
- Rewrote Step logic
- Enabled keyboard repeat events in tabgui
- Refactored NoRender settings
- Refactored ExtraChat mention settings
- Renamed ExtraChat "MentionIgnoreSelf" setting to "IgnoreSelfMsgs"
- Reduce amount of blocks that AutoTrap places
- Improved AutoTrap Minimal mode
- Made AutoMount donkey setting work with mules
- Improved AutoSurround Until Move mode
- HUD text alignment is now based on the quadrant the hud element is in, rather than the corner
- LogoutSpots now removes players if they log back in and you are not in their render distance
- Made WaterSpeed not work while elytra flying
- Renamed ClickGui setting "MaxPanelHeight" to "MaxHeight"
- *fakeplayer del command is no longer case sensitive
- Startup sounds are now randomly selected from StartupSounds folder

### Fixed

- *waypoints list command not displaying proper co-ordinates
- ExtraChat MentionIgnoreSelf setting not working
- BaseFinder checks using greater than rather than greater than or equals to
- Being able to open rusherhack guis while typing in a book
- FastPlace and ExpFast delay settings
- AntiPacket CPacketPlayer not cancelling subclasses
- Wither head Trajectories still being rendered while Airborne setting is disabled
- BreadCrumbs disappearing after you rubberband
- AutoTool switching to items that have the same effectiveness as your current item
- ElytraFly Vertical Jump option not working in Control mode
- AutoTool attack not working
- Speed module effecting elytrafly speed
- Autotrap and autosurround not being able to place blocks on blocks that open a gui
- Sneaking in freecam causing the player to dismount their riding entity
- BreakEsp self block only rendering if you are looking at the block
- Autoreconnect bug
- Trajectories inaccuracy on experience bottles
- Trajectories inaccuracy on fishing rods
- Entire hud resetting when there is one malformed setting
- Not being able to configure extrachest drop whitelist/blacklist with commands
- AutoTotem not working in GUIs
- NoSlow not working with AutoWalk
- Noslow not working with Baritone
- AutoTool not factoring in Efficiency enchantment
- Not being able to delete fakeplayers via command
- BlockOutline not outlining correct block while in freecam
- BlockOutline Depth setting and renamed it to DepthMask
- Entity interpolation on first tick
- Freecam rotating when trying to place/break blocks that are too far away from the player
- Search tracers bobbing if view bobbing is enabled
- Particles color leak
- AutoExp not working with non-english languages
- AntiHunger while mining
- Color leak in RangeCircle
- Nametags not displaying "max" for max enchanted elytra
- Clickgui and windows opening in guis that you don't want them to open in
- Autowalk walking the freecam player if riding an entity
- Tracers lighting bug
- Tracers being slightly off while view bobbing is enabled
- Freecam entity not showing absorption hearts of player
- MobOwner lagging game if the uuid is invalid
- NoGlitchBlocks breaking Scaffold
- AutoMine not working in GUIs and a Focused setting to change this
- BlockOutline causing vanilla chunk borders to be gray
- AutoTunnel attempting to mine liquid
- BlockOutline not working while in water
- SelfBlock not working with blocks over your head
- AutoTool attacking sand and gravel
- SelfBlock inconsistencies
- Inventory hud element items rendering over player list
- Aura attacking the entity you were riding
- NoFall bucket mode trying to place water in the nether
- *breed command not working with horses/donkeys
- Greeter delay
- NoRender Scoreboard setting
- FastBreak Packet mode breaking if you try to mine Bedrock
- LogoutSpots saying you have logged out if you went through 2b2t queue
- ExtraChat Mention Highlight resetting formatting
- CSGO Esp held item text not scaling properly to TextScale setting
- *kit delete creating a new kit
- not being able to open AntiPacket GUI in 2b2t queue
- ElytraFly InstantFly Timer mode slowing you down while in liquid
- AutoSurround not working properly while standing on an ender chest
- AutoEat not working while in guis
- AutoEat mode Both hunger taking priority
- Avoid Void setting not working while in liquid
- Not being able to add signs to Search
- Scaffold rendering state leak
- Typo in Strength detect in PvpInfo
- Typo in ExtraChest command

### Removed

- Removed delay on AutoExp
- Removed Seeker
- Removed AimAssist
- Removed ClickTP
- Removed HideCommon setting from PacketLogger
- Removed *antipacket gui

---

## [v1.1.3] - December 6th 2020

### Added

- ElytraFly mode Firework
- NoSlow 2b2t setting (glitchy sometimes)
- Particles module
- ExtraChat CustomFont setting
- AntiAFK setting to ElytraFly for Packet mode
- Gapples setting to HotbarReplenish
- Fireworks setting to HotbarReplenish
- FeatureList hud element Case setting
- BreakESP FillMode setting
- HoleESP void settings
- BoatFly ToggleOnDisconnect setting
- WaterSpeed Lava and LavaMultiplier settings
- FullBright Gamma number setting
- Freecam Rotate setting
- PacketLogger HideCommon setting
- "Add" button to alt manager
- [PLUS] Added EntityTeleportation setting to CoordLogger

### Changes

- BoatFly no longer turns while strafing left/right
- ExtraChest now works in non-chest containers
- Optimized RangeCircle rendering
- ".0" is now hidden from the end of sliders in the ClickGui
- When ClickGui's are first instantiated the panels now start from the far right to help people with small resolution monitors
- Neutral pigmen check is more accurate
- BreakESP now uses Interpolation for smooth rendering
- Rewrote WaterSpeed

### Fixed

- InventoryMove Strict setting
- Crash from main menu shader failing to compile on some systems
- ElytraFly packet mode not working as intended
- Not being able to use hand while riding boat with BoatFly
- Aura not working while riding
- Wither Skeletons not being detected as a hostile mob
- Fucker Lawn setting not working on grass
- Freecam not updating Direction hud element
- Waypoints color leak
- Waypoint beam not being accurate cross dimension
- Friends not saving bug from last patch
- AutoTunnel trying to break Bedrock
- High speed gain from using Speed Strafe while sneaking

---

## [v1.1.2] - November 10th 2020

### Added

- Criticals "Strict" setting
- Reset command alias "default"
- Waypoints "Vertical" setting
- ExtraChat "MentionIgnoreSelf" setting
- NoRender "RidingBoat" setting
- BoatFly "BoatScale" setting
- NoRender "FallingBlocks" setting
- NoRender "TileEntities" setting
- Interpolation to ClickGui sliders
- Inperpolation to ClickGui colors
- Baritone module "FreeLook" setting
- Baritone module "LogOnArrival" setting
- BoatFly "ConsecutiveLagBacks" setting (UNTESTED; setting it to 0 disables it)
- PvpInfo "32k Detect" setting
- HoleESP "CityRange" setting, for use with "CityESP"
- "OFF" option to Hud Notifications
- LogoutSpots "CustomFont" setting
- Waypoints "CustomFont" setting
- Second argument to toggle command to be able to specify whether you want the module to be enabled or disabled
- *watermark command

### Changes

- Save/load errors are now logged to "error_log.txt" file
- Rewrote most render methods
- Moved StartupSound setting from Hud to MainMenu module
- [PLUS] Rewrote MapReset

### Fixed

- Compatibility with Konas
- ExtraTab compatibility when using other clients with ExtraTab
- Button issue on MainMenu
- HoleESP FrustumCheck setting
- Corrupted configs while shutting down (I think)
- IP hud element not showing the server's ip if there was no port
- Rendering issues when not using Baritone
- Diagonal speed gain issue in Speed "Strafe"
- Console IndexOutOfBoundsException crash
- RotationLock not working in vehicles
- Mac users having to grant desktop access
- *kit command
- AutoWalk not working in vehicles
- Freecam causing kicks when using BoatFly
- LogoutSpots doubling
- Freecam mode "New" not using the player's health
- Custom Watermark not saving correctly

---

## [v1.1.1] - October 31st 2020

### Added

- 2b2t bypassing BoatFly setting "Strict" has been added to the normal version of the client
- CityESP setting to HoleESP
- Toggleable startup sound
- Ability to change the watermark text
- Height setting to NewChunks
- Depth setting to BlockOutline
- FillColorMode setting to Chams
- MacroList hud element
- PlayersOnly setting to EntityList hud element

### Changes

- [PLUS] Improved BowBomb
- Updated FAQ url on introduction screen

### Fixed

- AutoWeb
- Waypoints rendering cross dimension
- Fixed BaseFinder not working in boats
- SelfBlock still jumping if no blocks were in your hotbar
- HoleFiller trying to place blocks in holes players were in
- DeathFilter crash
- NullPointer crash in ClientSideTime
- FullBright not working correctly in vehicles
- Window and ClickGui blur not working on custom main menu
- 403 SSL issue when using some clients alongside rusherhack
- Failed to compile shader crash (hopefully)
- Main Menu shader breaking under certain conditions
- Bug where resizing minecraft window while using a rusherhack gui would not resize parent gui

---

## [v1.1] - October 24th 2020

### Added

- Loader now auto updates
- LongJump module
- AutoWeb module
- SelfBlock module
- ClientSideTime module
- Animations module
- DeathFilter module
- GlobalColors module to manage colors that multiple modules use
- Window system, you can use them in the Windows module
- Alt Manager window
- Console window
- Friend Manager window
- Ability to have multiple module profiles, *config command or the Profiles window
- *clear command
- *chat command
- *reloadsounds command
- New main menu shaders
- *reset command
- Comma setting to Position hud element
- Wither skulls to airborne Trajectories
- 2D mode to Tracers
- VisiblePredicate setting to ClickGui module (removes some settings if they are not used with your other settings)
- HealthItem setting to AutoTotem (offhand crystal)
- Strict setting to NoSwing
- Web setting to Avoid
- SetDead setting to AutoCrystal
- BreakHand setting to AutoCrystal
- 1.13+ setting to AutoCrystal
- Sync setting to AutoCrystal
- RandomMultiplier setting to AutoCrystal
- DeadTimeout setting to AutoCrystal
- Constantiam setting to ElytraFly
- Verbose setting to PacketLogger
- Shulker setting to ExtraTooltips
- [plus exlusive] Strict setting to BoatFly
- Size parameter to the customfont command
- Custom ttf file support to customfont command
- Value Alignment setting to the ClickGui module
- Rainbow setting to Trajectories
- Rainbow setting to Crosshair
- Save setting to ExtraScreenshot
- TotemCheck setting to AutoDisconnect
- HideF1 setting to Nametags
- FixYaw setting to BoatFly
- DropMode setting to ExtraChest
- ColorMode setting to PotionEffects hud element
- Forward setting to PlayerView hud element
- Port setting to Server IP hud element
- TotemPop setting to Notifications module
- OutlineThickness setting to Nametags
- Self setting to Nametags
- Range setting to Nametags
- Vanilla option to Speed mode
- PauseWhileEating setting to Aura
- RandomDelay setting to Spammer
- IgnoreSelf setting to BreakESP
- Scale setting to LogoutSpots
- Scale setting to Waypoints
- Scale setting to Hitmarkers
- Space setting to GreenText
- ElytraCheck setting to BaseFinder
- BuildHeight setting to BlockTweaks
- Resume setting to BaseFinder
- Notification setting to BaseFinder
- Texture setting to Chams
- /stats setting to AntiAFK
- Profile hud element

### Changes

- Rewrote the Garry's mod notifications, they are much smoother and don't desync
- Nametags CustomFont setting now works if you have the hud's customfont disabled
- Made module config save when you close the ClickGui
- You can open guis anywhere in the game now, example: in the server list
- Improved ClickGui blur
- Improved performance of ESP Outline mode
- Improved WaterSpeed
- Made PacketLogger disable on disconnect
- Setting values in the ClickGui are now light gray
- Rewrote Chams Wireframe mode
- Position hud element shows coordinates of render view entity instead of the player (now shows coords while using Freecam)
- LogoutSpots now get removed once the player logs back in
- AutoMine Exposed mode now checks if the block above is air
- Default Chams mode is now Fill
- *modules command now has darker colors if the module is not drawn in the FeatureList
- Long text in the ClickGui scrolls
- ClickGui clamp now only affects the X axis
- Cape users are now retrieved on another thread
- Renamed "Void" setting in Avoid to "Unloaded"
- Added void setting to Avoid which flags the anticheat if you are about to fall in the void
- Enabled keyboard repeating in console

### Fixed

- Main menu buttons appearing to be hovered over if you have a gui open
- *spammerfile command not printing usage correctly
- NoFall Packet mode
- Missing enchant glint when using Chams Color mode
- Chams not rendering items correctly
- Flickering sky when using the Weather setting in NoRender
- AutoTrap macro mode not disabling if your target left your range
- AutoNametag whitelist clear command clearing blacklist instead of whitelist
- BaseFinder travel mode off still autowalking
- LagDetector not abiding by the hud's customfont setting
- LogoutSpots module not serializing properly when saving
- ESP Csgo mode's armor not showing up if you are near a player in Freecam
- AutoCrystal targeting dead players
- ElytraFly pausing while using Freecam
- EntityControl NoPigAI stopping vertical movement
- Hitmarkers not working while using Aura
- ESP Boxes mode not using correct colors
- Being able to move the player while in Freecam with some Baritone actions
- Duplicating ClickGui
- AutoTool not using swords
- Timer not resetting sometimes while using Step Timer
- Step Timer lasting longer than it should
- Rare null pointer crash in the Ping hud element
- Greeter disabling after leaving a server

### Removed

- Source-styled console
- AutoDisconnect NoTotem setting
- ClassNotFoundException print if Baritone is not found

---

## [v1.0.2] - July 27th 2020

### Added

- Spectators setting to Nametags
- ClickGui scale setting
- FastBreak mode Packet
- Durability hud element
- Signs setting to Fucker
- IceSpeed
- Your current rusherhack version to RichPresence if you hover over the icon
- FakePlayer command

### Changes

- Speed mode strafe has less lagbacks (use strict setting on 2b2t)
- Improved AutoCrystal
- TabGui is no longer enabled by default
- TabGui animations are more smooth
- Hud clamping is now disable by default
- TabGui rainbow setting now enabled by default
- Removed shulkers from default search list
- AutoHole now pauses Speed
- Default AutoCrystal settings
- Your hand is now hidden in Freecam

### Fixed

- Text shadows not being drawn on element manager
- Fixed AutoWither
- AutoMine feet mode targetting friends
- AutoCrystal not placing if your AutoSwitch was off
- Scaffold not prioritizing your held item
- AutoTotem not switching last totem if you had a delay > 0
- No swing bobbing with SmallShield enabled
- Your hotbar not showing up in Freecam
- Height of the TabGui element
- RayTrace setting in AutoCrystal now works
- ElytraFly changing the timer speed while using freecam
- ESP Box mode bobbing if you have view bobbing enabled

---

## [v1.0.1] - July 20th 2020

### Added

- EntitySpeed
- Speed setting to WaterSpeed
- CustomFont setting to Nametags
- Hide setting to AutoReconnect (completely disables it in the disconnect screen if you use another client with auto reconnect)
- Return setting to AutoEat, returns to your previous slot after eating
- FastPlace

### Changes

- TextShadows have been added to the clickgui

### Fixed

- AutoCrystal not being able to place crystals with your offhand
- AutoCrystal AutoSwitch mode "Off" not working
- Freecam moving your player if you did not have baritone
- Sprint bug (I think, was unable to reproduce)
- NoFall mode Anti not removing flying effect
- Typo in the AntiBan description
- Nametags causing all vanilla nametags (including non player nametags) to vanish
- Rotations conflicting with Future Client
- Compatibility with Summit client

---

## [v1.0.0] - July 2nd 2020

### Added

- Render setting to LagDetector
- Extracraft, autocraft module recipe can be set with *recipe set
- Recipe command, *recipe get will tell you how to craft an item, *recipe list for a list
- Added regear (module to automatically regear from a shulker, save a kit with *createkit and select a current kit with *selectkit
- ID commmand, use *id or *id to get item ids
- Translate module, use *language to set the languages, my refers the the language that other's messages will be translated to, participants is the language that you will translate your messages to
- CSGO ESP mode
- Potion setting to Fullbright
- HotbarReplenish
- Distance setting to ViewClip
- Angles setting to RotationLock
- CaveFinder
- Look and LookSpeed setting to InventoryMove
- Ability to bind modules to mouse buttons (only available via commands right now, *bind add mouse(number) module, example: *bind add mouse5 criticals
- Some modules that change your rotation will now allow you to see where its rotating if you are in third person
- AutoReconnect
- AutoWither
- AutoNametag and autonametag command
- BossStack
- Delay setting to RichPresence
- Server ip setting to RichPresence
- Notification system
- Added console, default key to open the console is ` (grave)
- HitboxIgnore (ignores player hitboxes while trying to mine, place, etc)
- BreakESP, highlights blocks being broken
- Basic Baritone integration
- Avoid
- Sprint Omnidirectional setting, and a strict setting that should bypass all anticheats
- Introduction screen when you run rusherhack for the first time
- Update screen when the client updates itself
- Settings to RainbowEnchant
- AutoHole (baritone module)
- HoleFiller
- Baritone module
- Added Fly mode to AntiLevitation
- Added settings to noglitchblocks
- CastDelay setting to AutoFish
- CustomFont rendering, change the font with *customfont
- Added custom main menu with custom shader backgrounds, customize it with the mainmenu module (you can toggle it off too)
- RangeCircle
- (Plus Only) Added Boatfly Bypass (strict setting)
- Added Bedspawn command
- WayPoints

### Changes

- Combine NoChatBackground, NameHighlight, Nameprotect, NoChat, and MaxChatLines into a new module called "ExtraChat"
- Directory has been changed from .minecraft/rusher_hack/ to .minecraft/rusherhack
- Rewrote Announcer
- Combine DeathAnnouncer and Autocityboss into "AutoToxic"
- Rewrote Nametags
- Rewrote AutoReply
- RusherCrypt, RusherDecrypt, and ChatObfuscator combined into one module "RusherCrypt"
- Rewrote LogoutSpots and moved it to render
- Merged SignText and colorsigns into one module "ExtraSign", added date append setting
- Rewrote Spammer with the ability to have more than 1 spammer config, *spammerfile command
- Merged StrengthDetect and VisualRange into PvpInfo and added and Pearls
- Rewrote Trajectories
- Rewrote aimbot and renamed it to AimAssist
- Rewrote KillAura and renamed it to Aura
- Merge Antishulker and HopperNuker into Fucker and added rotations and delay setting
- Rewrote AutoArmor and added blastprot priority, elytrapriority, and delay settings
- Rewrote AutoCrystal and added a lot of settings
- Moved Velocity to movement category
- Rewrote Velocity and merged NoPush into velocity with more customizability
- Rewrote NoSlow and merged NoSlip and NoWeb into NoSlow and added soulsand and strict setting
- Merged all storage settings in esp into one setting called "Storages"
- Rewrote AutoExp with dynamicarmor setting
- Rewrote autototem and added soft setting
- Rewrote AutoObsidian and renamed it to AutoSurround, added a lot of settings and fixed a lot of bugs
- Rewrote NoRender and added more settings
- Rewrote Criticals
- (Plus Only) Merged bowbomb into bowspam
- Move Timer to world category
- Improved strafe speed, and removed useless modes
- Merged Strafe module into speed as a mode called "GroundStrafe"
- Rewrote HoleESP
- Merge NoWeather into NoRender
- Renamed DebugCrosshair to Crosshair and added csgo mode with a lot of options
- Remade bind command, bind
- Rewrote AutoTrap with tons of new features
- Rewrote BowAim and renamed it to BowAimbot
- Merged LawnMower into Fucker as the setting "Lawn"
- Rewrote TriggerBot with more settings
- Merged NoCaveCulling into NoRender as "CaveCulling" setting
- Renamed Flight mode Static to Creative
- Made RotationLock smoother
- Rewrote Xray
- Rewrite InventoryMove (now compatible with more clients)
- Rewrote Scaffold, bypasses ncp now
- Rewrite tracers, more settings
- Improved PacketFly, desyncs less often but it still cannot phase easily
- Rewrite AntiAim
- Improve NoForceRotate
- Rewrote AutoMount
- Rewrote FastBreak and added speed and delay setting
- Replaced color settings in modules with a color picker
- Rewrote jesus, added solid mode
- Rewrote ElytraFly (replaced 2b2t mode with control, can be used to go upwards. fixed packet)
- Merge novoid into avoid
- Rewrote newchunks, added settings
- Rewrote BaseFinder
- Rewrote AntiHunger
- Rewrote Freecam, now compatible with baritone
- Rewrote BoatFly
- Rewrote Chams, WAY more settings
- Rewrote SkinBlink
- Rewrite AntiAFK with baritone setting
- Rewrote AutoEat, should work better in low tps environments
- Merged AutoGapple into AutoEat as health mode
- Rewrote Breadcrumbs
- Rewrote AutoMine (now has a mode to mine blocks at players feet so you can easily crystal them)
- Renamed "Other" category to "HUD"
- Rewrote AntiPacket
- Renamed portalchat to portalgui
- Rewrote clicktp
- renamed Gui category to Client
- AutoEat now pauses baritone pathing (toggleable)
- BaseFinder now prints the server ip in the log
- Rewrote Zoom
- Rewrote search
- Renamed MiddleClickFriends to MiddleClick, added range setting, entitynbt setting, and blocknbt setting
- Rewrote PacketMine and renamed it to NoMineAnimation
- Rewrote autotunnel
- Rewrote LiquidRemover, renamed it to SourceRemover
- Rewrote Nuker
- Rewrote Ignite, moved to combat category
- Rewrote BlockOutline
- Rewrote Hitmarkers, added customizable sound (replace hitmarker.ogg in .minecraft/rusherhack/Hitmarkers with a file with the same name and extension)
- Rewrote AutoSpleef
- Rewrote Phase
- Rewrote NoFall and moved to movement category
- Rewrote the ClickGui (removed scale slider since it scales automatically)
- Rewrote HUD, default hud editor keybind is comma
- Rewrote every HUD element#
- Merged AutoQueueReconnect into AutoReconnect as a setting
- Rewrote GameMode
- Renamed ImgurScreenshot to ExtraScreenshot
- Rewrote Notifications module
- Rewrote PingSpoof (it actually works now)
- Moved MapReset to misc category
- Rewrote Lagger and added new modes
- Moved Lagger to misc category
- Rewrote ChestStealer, renamed it to ExtraChest, and moved it to misc category
- Moved AntiLagExploit to misc and renamed it to NoSoundLag
- Rewrote Borders module, add settings for chunks, mapart, and regions and ylevel
- Rewrote Seeker
- Renamed Desync module to EntityDesync
- Rewrote every command
- Rewrote MobOwner
- Rewrote macro system

### Fixed

- A bug in ChatAppend where you couldn't use unicode text
- "MoorseCode" typo in FancyChat
- Probably fixed weird chunk bug with baritone
- Improved performance of render modules
- AutoRespawn deathcoords no longer spams chat
- Grey ESP boxes if using the client with baritone
- Some HUD elements hot having text shadow
- Fixed BaseFinder crashes
- AutoWalk compatibility with other clients
- Jesus and Step now work with baritone
- Compatibility of BlockTweaks with other clients
- Fix ForcePlace
- Fixed multimc compatibility

### Removed

- Disability module (it can just be done with ChatAppend lol)
- popbobLag and clydeLag
- NameBypass because hause's patch was removed
- StrengthDetect
- Anti32k
- Auto32k
- AutoElytraReplace (use elytrapriority in AutoArmor)
- AutoChorus
- Flight modes Weird and Hypixel
- Rewrote AutoAccept and add setting for duels
- Headless module
- RemoveCrystal
- PullBack
- AutoGapOffhand
- BoatClip
- Heaven
- NoLagDesync
- Rewrote Xcarry and merged IllegalItemBypass into Xcarry as "Cancel" setting
- Rewrote CoordLogger
- Australia
- HitSpheres
- HopperRadius
- removed Promod

---
