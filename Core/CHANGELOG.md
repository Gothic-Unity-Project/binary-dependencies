# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.8.0] - 2026-10-11

### Added
- NVorbis.dll (v0.10.5, MIT) - managed Ogg Vorbis decoder used for mod dubbing (moved from Gothic-Unity/Assets/Plugins/NVorbis)
- License files for every bundled component (ZenKitCS, ZenKitCAPI, dmusic, dmusic-cs, NVorbis, Mono I18N)

### Changed
- Each dependency now lives in its own folder (`ZenKit/`, `dmusic/`, `NVorbis/`, `I18N/`) next to its license file(s). `.meta` GUIDs are unchanged.

## [1.7.0] - 2026-05-09

### Added
- Additional ZenKit features for
    - GetInstance/SetInstance (https://github.com/GothicKit/ZenKitCS/issues/25)
    - OffsetAsMember/ClassSize (https://github.com/GothicKit/ZenKitCS/issues/24)
    - IsTopOfStackReference/PopReference (https://github.com/GothicKit/ZenKitCS/issues/23)
    - JumpUnsafe/ProgramCounter (https://github.com/GothicKit/ZenKitCS/issues/22)


## [1.6.0] - 2026-03-01

### Added
- Additional ZenKit modding features like _UseAccessTrap_, _SetAccessTrapCallback_ and _DaedalusTransientInstance_


## [1.5.0] - 2026-01-31

### Updated
- bumping latest ZenKit*.dll files
- e.g., Improves loading of Gothic data into memory: only when accessed inside ZenKit for the first time (needed for large mods to speed up loading from minutes to seconds.)


## [1.4.0] - 2025-09-26

### Added
- Linux x86 dependencies for working with Unity Editor on Linux


## [1.3.0] - 2025-08-28

### Added
- Reflex (DI framework) SceneScope to enable DI on world scenes.


## [1.2.8] - 2025-08-21

### Updated
- bumping latest ZenKit*.dll files
- Adds (e.g.,) DEF_HIT_LIMB properties for Animation to C# interface.


## [1.2.7] - 2025-06-01

### Fixed
- MenuItemInstance.GetText(i) is now using the passed index (https://github.com/GothicKit/ZenKitCAPI/issues/4)


## [1.2.6] - 2025-02-15

### Updated
- Occlusion Culling data for G1 worlds.


## [1.2.5] - 2025-02-09

### Updated
- Fog values for world.zen.


## [1.2.4] - 2024-11-02

### Fixed
- Game crashed when SaveGame contained zCEventManager data.


## [1.2.3] - 2024-10-13

### Fixed
- TextureBuilder won't crash when GC'd.


## [1.2.2] - 2024-10-13

### Fixed
- Initializing multiple NpcInstances of same Index work correctly.


## [1.2.1] - 2024-10-07

### Added
- NpcInstance (subclass of DaedalusInstance) contains UserData field to store exchangeable data between ZenKit's objects and UnZENity ones.


## [1.2.0] - 2024-09-22

### Fixed
- Daedalus externals where strings are sent to ZenKit are encoded correctly.

### Added
- Interfaces for all Vob types inside ZenKitCS added (I*VirtualObject). https://github.com/GothicKit/ZenKitCS/pull/12


## [1.1.2] - 2024-09-20

## Updated
- All scenes now have a Bootstrapping GameObject+Component attached (WorldSceneManager.cs). It will get called whenever the scene is loaded.


## [1.1.1] - 2024-09-15

### Fixed
- Daedalus support for _null_ return values when a class is expected (e.g. Hlp_GetNpc(); https://github.com/GothicKit/ZenKitCS/issues/10)
- Daedalus support for DaedalusInstance as parameters for _overloaded_ external calls like Hlp_GetInstanceID() (https://github.com/GothicKit/ZenKitCS/issues/8)


## [1.1.0] - 2024-08-31

### Updated
- Occlusion data for Gothic1 worlds.
- Moved occlusion data into subfolder.

### Added
- Occlusion data for Gothic2 Night of the Raven worlds.


## [1.0.5] - 2024-08-10

### Fixed
- Non-void Daedalus function calls without a proper return value always provide default return values.


## [1.0.4] - 2024-08-04

### Added
- VOBs of type _oCNPC_ can be casted to _ZenKit.Vobs.Npc_ directly.


## [1.0.3] - 2024-07-02

### Added
- Items (VOBs) now contain fields for _Amount_ and _Flags_ from save files.


## [1.0.2] - 2024-06-29

### Fixed
- Fixes multiple issues with file loading on Windows which caused Vfs mounting to fail in various places.


## [1.0.1] - 2024-06-23

### Fixed
- Zen worlds loading inside a SaveGame returns null instead of a segfault.


# [1.0.0] - 2024-06-01

### Added
- Initial commit.
