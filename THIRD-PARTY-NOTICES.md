# Third-Party Notices

SpaceSim is released under the MIT License (see [LICENSE](LICENSE)). It **bundles**
the third-party components listed below, each of which remains under its own
license. These notices must travel with the game whenever it is redistributed —
they are included in the release download alongside `SpaceSim.exe`.

Each library is shipped as a **separate, unmodified dynamic library (DLL)** next to
the executable. Nothing here is statically linked into SpaceSim, and any of these
DLLs may be replaced with a compatible build by whoever has a copy of the game.
That matters for the LGPL components below, whose licenses require exactly that
freedom.

---

## Screen-reader support

### Tolk
The screen-reader abstraction layer that lets SpaceSim speak through NVDA, JAWS,
SAPI and others. Shipped as `Tolk.dll` and `TolkDotNet.dll`.

- Copyright © Davy Kager
- License: **GNU Lesser General Public License, version 3 (LGPL-3.0)**
- Source: https://github.com/dkager/tolk

### NVDA Controller Client
The client library Tolk uses to talk to the NVDA screen reader. Shipped as
`nvdaControllerClient64.dll`.

- Copyright © NV Access Limited and contributors
- License: **GNU Lesser General Public License, version 2.1 (LGPL-2.1)**
- Source: https://github.com/nvaccess/nvda

---

## Audio

### OpenAL Soft
The spatial-audio engine providing HRTF positioning for the world soundscape.
Shipped as `OpenAL32.dll`.

- Copyright © Chris Robinson and contributors
- License: **GNU Library General Public License, version 2** (as shipped in the
  project's `COPYING` file; commonly referred to as LGPL-2.x)
- Source: https://github.com/kcat/openal-soft

### NAudio
Real-time audio synthesis and WASAPI output for the resonance drives.

- Copyright © Mark Heath and contributors
- License: **MIT**
- Source: https://github.com/naudio/NAudio

---

## Game framework

### MonoGame (MonoGame.Framework.DesktopGL)
The application/game host and windowing layer.

- Copyright © The MonoGame Team; portions © The Mono.Xna Team
- License: **Microsoft Public License (Ms-PL)**; portions under the **MIT License**
- Source: https://github.com/MonoGame/MonoGame

### SDL2
The cross-platform windowing/input backend used by MonoGame DesktopGL. Shipped as
`SDL2.dll`.

- Copyright © Sam Lantinga and contributors
- License: **zlib License**
- Source: https://github.com/libsdl-org/SDL

### OpenTK
The managed bindings used to drive OpenAL.

- Copyright © The Open Toolkit contributors
- License: **MIT**
- Source: https://github.com/opentk/opentk

---

## Runtime

### .NET Runtime
SpaceSim ships as a self-contained application, so the .NET runtime libraries are
included in the download.

- Copyright © .NET Foundation and Contributors
- License: **MIT**
- Source: https://github.com/dotnet/runtime

---

## A note on the LGPL components

Tolk, the NVDA Controller Client, and OpenAL Soft are covered by the GNU Lesser
General Public License. SpaceSim uses them the way the LGPL intends: they are
separate DLLs loaded at runtime, not compiled into the game. If you wish to use a
modified version of any of them, you may simply replace the corresponding DLL in
the game folder with your own compatible build. Full license texts are available
at the source links above, and from the Free Software Foundation at
https://www.gnu.org/licenses/.

If you spot an error or omission in these notices, please open an issue — getting
attribution right matters, and corrections are welcome.
