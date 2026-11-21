# SugarClient 1.21.11

A modular Minecraft Java client mod built with Fabric and Java 21.

## Project status

- Minecraft: 1.21.11
- Loader: Fabric
- Java: 21
- Main package: `dev.sugarexploit.client`
- Mod ID: `sugarexploit_client`

The framework foundation and first interactive GUI are now in the repository. Compilation and in-game testing are still pending; this is not yet a finished release JAR.

## Where the modules are

The folders have different purposes:

- `module/Module.java`: abstract base class shared by all modules.
- `module/ModuleManager.java`: registers modules and ticks enabled modules.
- `module/Category.java`: module categories.
- `module/impl/`: concrete, usable module implementations. The first one is `ToggleSprintModule.java`.
- `setting/`: generic, boolean, and numeric settings.
- `ui/ClickGuiScreen.java`: in-game module screen.

So the actual modules are not mixed into `Module.java`: each module belongs in its own Java file under `module/impl/`.

## Current controls

- Press **Right Shift** in-game to open the SugarClient GUI.
- Click a module row to turn it ON or OFF.
- Current implemented module: **ToggleSprint**.

## Build

The project uses Gradle and Fabric Loom. Run:

```sh
./gradlew build
```

The mod JAR is expected in `build/libs/` after a successful build.

## Next milestones

1. Confirm the project builds on the GitHub Actions runner.
2. Add the ArrayList HUD and configurable ClickGUI.
3. Add further modules in separate files under `module/impl/`, with settings where appropriate.

The architecture specification is the design reference. Features are added in stages and are not marked complete until implemented and tested.


## Cloud build

GitHub Actions compiles this project on pushes to `main` using Java 21. The successful `SugarClient-JAR` artifact is available from the workflow run's Artifacts section.
