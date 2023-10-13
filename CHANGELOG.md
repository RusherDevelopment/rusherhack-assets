# Changelog
All notable changes to RusherHack be documented in this changelog.

---

## [Unreleased]

## [v2.0-preview] - October 7th 2023

- v2.0 is an almost complete overhaul of rusherhack for modern versions of the game.
- Previous versions of rusherhack are referenced to as "legacy" versions.

- This version is still in development, however an early access preview is released.
  - Not all features from legacy rusherhack versions have been implemented yet, but are planned to.


### Added

- Rotations Module
  - MoveFix used on 2b2t or other servers with similar anticheats.

- CustomFont module
  - Allows you to easily control the settings of the custom font renderer.

- Theme module
  - Control theme-specific settings, such as Color.
  - Will be expanded upon with custom themes.

- UI / Graphics
  - Added screen selector to the right side of all rusherhack screens.

- Hud
  - Added resizeable hud elements.
    - Can be scaled by dragging the bottom right corner of said hud elements.
  - Added a visual representation for snap points whilst in the Hud Editor.
  - Added snap point at the top-center of the screen.
  - Added visual representation for empty list hud elements whilst in the Hud Editor

- Commands
  - Added command suggestions for command arguments.

######

- Git commit hash to watermark for beta testers

### Fixed

- 1
- Ping hud element not working on 2b2t.


### Changed

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

- Bind System
  - Binds are now stored in their own folder, separate from module configs.

- Macro System
  - Macros can now be named and are now configured by the name of the macro, instead of the key.
  - Macros can now have multiple commands added.

- Config System
  - The format for all configs have been changed since legacy versions.
  - Configs now automatically save every 5 minutes.

######
- Rotations have been vastly improved
- MacroList hud element has been updated to improve the representation of the new macro system.
- Moved Capes setting from the Hud module into its own module.
- Updated *credits command.


### Removed

- EntityDesync module
- PacketFly module
- Dismount command

---

Legacy changelogs (before version v2.0) (PUT LINK HERE).
