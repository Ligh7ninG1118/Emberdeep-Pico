# Emberdeep

Emberdeep is a hand-tracked tabletop firefighting game for PICO and Meta Quest. A miniature forest sits on the table in
front of you, and a fire is coming. Open your palm to aim and spray water, hammer the pump with your fist to refill your
gem, read the wind and the forecast, place water towers while time stands still, and save the sheep. It is played
seated, with hands only, in English and Simplified Chinese.

This repository is the source snapshot of the PICO store release **1.0.0** (versionCode 32, package
`com.metahackathon2026.emberdeep`). It holds the Emberdeep project only. Code from the shared hackathon workspace that
Emberdeep compiles against is included, but the other games' scenes and art are not.

Original team repository: https://github.com/biggermelon3/emberdeep

## Open and build

- Unity **6000.3.21f1**, Android build target.
- Scenes: `Assets/FireRescue/Scenes/EmberdeepCamp.unity` (camp, menu, tutorial) and `EmberdeepFireground.unity` (levels).
- PICO APK: menu **Emberdeep > Build PICO APK** (`Builds/Emberdeep-Pico.apk`). Quest: **Emberdeep > Build Quest APK**.
  Command line: `Unity.exe -batchmode -quit -projectPath . -buildTarget Android -executeMethod FireRescue.Editor.EmberdeepQuickBuild.BuildFromCommandLine -pico`
- The PICO OpenXR SDK comes from its public git URL (see `Packages/manifest.json`).
- Store builds are re-signed with the release key afterwards. The key is not in this repository.

## Layout

- `Assets/FireRescue/`: the game (runtime, editor tools, art, voice, localization, tests).
- `Assets/MetaHackthone/`, `Assets/CloudGarden/`, `Assets/ShadowWorkshop/`: shared rig, input and build code from the
  hackathon workspace.
- `Docs/Emberdeep/`: design and engineering notes.

## Third-party

- Noto Sans CJK SC: SIL Open Font License 1.1.
- Sky photograph: Poly Haven, CC0.
- Unity packages, Meta XR SDK and PICO OpenXR SDK: under their own licences, pulled by the package manager.
