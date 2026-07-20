LightZone
=========

Flatpak for LightZone.

https://github.com/ktgw0316/LightZone

Uses JAVA 21.

Permissions
-----------

File system permissions:

- `xdg-pictures`: because this doesn't support portals
- persist: two directories left by Java that we think should be
  persisted.


Other

- X11 only
- Added DRI, albeit not sure it uses it.

Other
-----

Source is from git because submodules are needed.

`lensfun` is installed, directly lifted from Darktable flatpak.

`javahelp2` is needed but not provided with dependencies. Seems that
it's put in the right location.

To generate `flatpak-sources.json` (a list of required jar files),
run `./gradlew flatpakGradleGenerator --no-configuration-cache`
in the LightZone source code directory.
(See https://github.com/jwharm/flatpak-gradle-generator for more information.)
The flatpak-gradle-generator can't list gradle-bin.zip and some of the plugin jars,
so they should be manually added into `flatpak-plugin-sources.json`.

Fonts look ugly. Maybe it's just Java.
