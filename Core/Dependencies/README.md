This project relies on the following dll/so libraries. Each component lives in its own folder together with
its license file(s).

| Folder     | Files                                                     | License                    |
|------------|-----------------------------------------------------------|----------------------------|
| `ZenKit/`  | ZenKit.dll, zenkitcapi.dll, libzenkitcapi.so              | MIT (incl. libsquish, mio) |
| `dmusic/`  | dmusic.dll, libdmusic.so, DirectMusic.dll                 | MIT (Modern Variant)       |
| `NVorbis/` | NVorbis.dll (v0.10.5)                                     | MIT                        |
| `I18N/`    | I18N.dll, I18N.MidEast.dll, I18N.Other.dll, I18N.West.dll | MIT (Mono)                 |

* ZenKit.dll - Managed .NET library (https://github.com/GothicKit/ZenKitCS); can be used on linux systems as well;
  _extern_ bridge between libzenkitcapi and Unity
* zenkitcapi.dll / libzenkitcapi.so - Unmanaged C library (https://github.com/GothicKit/ZenKitCAPI) wrapping
  ZenKit (https://github.com/GothicKit/ZenKit); actual Gothic asset parser logic. Statically includes libsquish
  and mio.
* dmusic.dll / libdmusic.so - DirectMusic reimplementation (https://github.com/GothicKit/dmusic)
* DirectMusic.dll - Managed .NET bindings for dmusic (https://github.com/GothicKit/dmusic-cs)
* NVorbis.dll - Managed .NET library (https://github.com/NVorbis/NVorbis); Ogg Vorbis decoder for mods shipping
  dubbing as .ogg
* I18N.*.dll - Managed .NET library from Mono. Required to get Windows codepages inside builds. Taken from
  _INSTALL_DIR\Unity\Hub\Editor\VERSION\Editor\Data\MonoBleedingEdge\lib\mono\gac\*_
* link.xml - Prevents IL stripping of the I18N assemblies on arm64 builds


libzenkitcapi / libdmusic OS specific versions:
* .dll - Windows version
* .so - arm64 version
* linux_x86/*.so - Linux x86 version for working with the Unity Editor on Linux (Hint: OpenXR plugin isn't
  compatible with Linux runtimes. Development on this system might be cumbersome:
  https://docs.unity3d.com/Packages/com.unity.xr.openxr@1.7/manual/index.html)
* .dylib - (not used!) MacOSX version (Showed error "Cannot set deprecated build target 'OSXIntel', therefore not
  added right now)


I18N.*.dll:
* I18N - General language support
* I18N.MidEast - Windows-1250 codepage
* I18N.Other - Windows-1251 codepage
* I18N.West - Windows-1252 codepage
