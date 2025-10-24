# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.6.2] - 2025-10-24

### Fixed

- Fixed optional ModAPI dependencies [#38] @zimuya4153

## [0.6.1] - 2025-10-22

### Fixed

- Fixed the console screen flooding output [#37] @zimuya4153

## [0.6.0] - 2025-10-22

### Changed

- Adapted to LeviLamina 1.6.x and bds 1.21.111.1 @zimuya4153

## [0.5.0] - 2025-10-13

### Changed

- Adapted to LeviLamina 1.5.x and bds 1.21.102.1 [#35] @zimuya4153

### Fixed

- Fixed the issue of the Chinese path in the ResourcePackDownloadFix feature @zimuya4153
- Fixed the global formatting issue of ChatFormatter [#32] @zimuya4153

## [0.4.0] - 2025-07-17

### Changed

- Adapted to LeviLamina 1.4.0 and bds 1.21.93.1 @zimuya4153
- Modify the command config of the ScheduleTask function to an array @zimuya4153
- Refactor the ExperimentsEditor function @zimuya4153

### Removed

- Remove the permissions that are not useful for the CommandMap function @zimuya4153

## [0.3.1] - 2025-07-16

### Fixed

- Fixed FastLeafDecay feature [#26] @zimuya4153

## [0.3.0] - 2025-06-12

### Changed

- Adapted to LeviLamina 1.3.0 and bds 1.21.80.03 @zimuya4153

## [0.2.1] - 2025-06-12

### Added

- Added XpOrbMerge feature @zimuya4153
- Added CostTime class @zimuya4153
- Added CostTime to some features @zimuya4153
- Added log_level to Config @zimuya4153

### Changed

- Adapted LeviLamina 1.2.0 and BDS 1.21.70.04 @zimuya4153

### Fixed

- Fixed performance issue of the CleanerUnknownBlock feature [#23] @zimuya4153
- Fixed crash for loading config file @zimuya4153

## [0.1.2] - 2025-06-01

### Added

- Added ChatFormatter feature [#10] @zimuya4153
- Added config backup on loadConfig failure [#17] @zimuya4153
- Added BanBuff feature [#15] @zimuya4153
- Added DimensionDisablingCommand feature [#14] @zimuya4153
- Added BanEntity feature [#20] @zimuya4153

### Changed

- Remove the useless judgments @zimuya4153
- Enhance CommandMap feature [#22] @zimuya4153

### Fixed

- Fixed AutoReload feature [#8] @zimuya4153
- Fixed the issue where the event could not be intercepted @zimuya4153
- Fixed README.md and README.zh.md typo [#16] @zimuya4153
- Fixed the failure of the ChatFormatter function reactivate @zimuya4153

## [0.1.1] - 2025-05-21

### Added

- Added ResourcePackDownloadFix feature @zimuya4153
- Added FakeMotd feature @zimuya4153
- Added ScheduleTask feature @zimuya4153
- Added QuickCmdGui feature [#4] @zimuya4153
- Added CommandMap feature @zimuya4153
- Added FarmLandProtect feature [#5] @zimuya4153
- Added DynamicMotd feature [#1] @zimuya4153
- Added AutoReload feature [#7] @zimuya4153
- Added DeathLootDimension feature [#6] @zimuya4153
- Added ChatRecord feature @zimuya4153
- Added ExperimentsEditor feature @zimuya4153
- Added AddonLoader feature @zimuya4153

### Changed

- Changed the i18n translation to the client resource package translation @zimuya4153
- Refactor FastLeadDecay feature @zimuya4153
- Refactor restructure directories and mod packer @zimuya4153

### Fixed

- Fixed InvisibleOP feature [#3] @zimuya4153
- Fixed ForceEducationEdition feature blocking client/server access @zimuya4153
- Fixed ForceEducationEdition feature not activating during archive initialization @zimuya4153

## [0.1.0] - 2025-05-04

### Added

- Added AutomaticFishing feature @zimuya4153
- Added CleanerUnknownBlock feature @zimuya4153
- Added ContainerReader feature @zimuya4153
- Added CoResourcePack feature @zimuya4153
- Added CustomCmdAlias feature @zimuya4153
- Added CustomCmdPermission feature @zimuya4153
- Added DoubleDoor feature @zimuya4153
- Added ExplosionModify feature @zimuya4153
- Added FakePlayerNoSleep feature @zimuya4153
- Added FakeSeed feature @zimuya4153
- Added FakeWorldName feature @zimuya4153
- Added FastLeafDecay feature @zimuya4153
- Added ForceAchievements feature @zimuya4153
- Added ForceEducationEdition feature @zimuya4153
- Added ForceRegisterAbilityCmd feature @zimuya4153
- Added Gamemode6Fix feature @zimuya4153
- Added InvisibleOP feature @zimuya4153
- Added TrustedSkin feature @zimuya4153
- Added BlockModifyPermissions feature @KobeBryant114514
- Added LockWorldSettings feature @KobeBryant114514
- Added ServerSettingsUI ui @zimuya4153 @KobeBryant114514

[#1]: https://github.com/GroupMountain/GMEssentials-Release/issues/1
[#3]: https://github.com/GroupMountain/GMEssentials-Release/issues/3
[#4]: https://github.com/GroupMountain/GMEssentials-Release/issues/4
[#5]: https://github.com/GroupMountain/GMEssentials-Release/issues/5
[#6]: https://github.com/GroupMountain/GMEssentials-Release/issues/6
[#7]: https://github.com/GroupMountain/GMEssentials-Release/issues/7
[#8]: https://github.com/GroupMountain/GMEssentials-Release/issues/8
[#10]: https://github.com/GroupMountain/GMEssentials-Release/issues/10
[#14]: https://github.com/GroupMountain/GMEssentials-Release/issues/14
[#15]: https://github.com/GroupMountain/GMEssentials-Release/issues/15
[#16]: https://github.com/GroupMountain/GMEssentials-Release/issues/16
[#17]: https://github.com/GroupMountain/GMEssentials-Release/issues/17
[#20]: https://github.com/GroupMountain/GMEssentials-Release/issues/20
[#22]: https://github.com/GroupMountain/GMEssentials-Release/issues/22
[#23]: https://github.com/GroupMountain/GMEssentials-Release/issues/23
[#26]: https://github.com/GroupMountain/GMEssentials-Release/issues/26
[#32]: https://github.com/GroupMountain/GMEssentials-Release/issues/32
[#35]: https://github.com/GroupMountain/GMEssentials-Release/issues/35
[#37]: https://github.com/GroupMountain/GMEssentials-Release/issues/37
[#38]: https://github.com/GroupMountain/GMEssentials-Release/issues/38

[Unreleased]: https://github.com/GroupMountain/GMEssentials/compare/v0.6.2...HEAD
[0.6.2]: https://github.com/GroupMountain/GMEssentials/compare/v0.6.1...v0.6.2
[0.6.1]: https://github.com/GroupMountain/GMEssentials/compare/v0.6.0...v0.6.1
[0.6.0]: https://github.com/GroupMountain/GMEssentials/compare/v0.5.0...v0.6.0
[0.5.0]: https://github.com/GroupMountain/GMEssentials/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/GroupMountain/GMEssentials/compare/v0.3.1...v0.4.0
[0.3.1]: https://github.com/GroupMountain/GMEssentials/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/GroupMountain/GMEssentials/compare/v0.2.1...v0.3.0
[0.2.1]: https://github.com/GroupMountain/GMEssentials/compare/v0.1.2...v0.2.1
[0.1.2]: https://github.com/GroupMountain/GMEssentials/compare/v0.1.1...v0.1.2
[0.1.1]: https://github.com/GroupMountain/GMEssentials/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/GroupMountain/GMEssentials/releases/tag/v0.1.0
