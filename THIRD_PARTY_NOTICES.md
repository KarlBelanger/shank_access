# Third-party notices

Shank Access's own code is under the MIT licence (LICENSE). It uses and ships these components, each under its own
licence. The full licence texts are in the `licences` folder of the release (and in `third_party/` in the source).

## In the mod (bin/)

- **MinHook 1.3.4** (function hooking, compiled into shank_access.dll and dinput8.dll). Copyright (C) 2009-2017
  Tsuda Kageyu. BSD 2-Clause licence: `third_party/minhook/LICENSE.txt`. https://github.com/TsudaKageyu/minhook
- **miniz 3.1.2** (zip files of a session's logs, compiled into shank_access.dll). Copyright 2013-2014 RAD Game Tools
  and Valve Software, Copyright 2010-2014 Rich Geldreich and Tenacious Software LLC. MIT licence:
  `third_party/miniz/LICENSE`. https://github.com/richgel999/miniz
- **Tolk** (screen reader output; Tolk.dll, unmodified). Copyright (C) 2014-2016 Davy Kager. GNU LGPL 3.0:
  `third_party/tolk/LICENSE.txt`. Source: https://github.com/dkager/tolk. Tolk.dll is a separate DLL; you may
  replace it with your own build of Tolk.
- **NVDA Controller Client** (nvdaControllerClient32.dll, unmodified, as distributed with Tolk). Copyright (C) NV
  Access Limited. GNU LGPL 2.1: `third_party/tolk/LICENSE-NVDA.txt`. https://www.nvaccess.org
- **System Access API** (SAAPI32.dll, Serotek) and **Dolphin SuperNova API** (dolapi32.dll, Dolphin Computer Access),
  unmodified, redistributed as part of Tolk under their vendors' terms for Tolk.

## In the setup program (shank-access-setup.exe)

- **Python 3** (the bundled interpreter). PSF License Agreement. https://www.python.org
- **PyInstaller 6** bootloader (packs the setup program). GPL 2.0 with the bootloader exception, which allows
  distributing the bundled program under any licence. https://pyinstaller.org
- **lupa** (Lua in Python, to read the game's level scripts). MIT licence. https://github.com/scoder/lupa ; it includes
  **Lua** (MIT licence, Copyright (C) 1994-2024 Lua.org, PUC-Rio).
- **path_graph.exe** is Shank Access's own code (MIT).

## Development tools only (not shipped)

- **Lua 5.0.3** (checking the game's Lua 5.0 scripts). MIT licence: `third_party/lua-5.0.3/COPYRIGHT`.
