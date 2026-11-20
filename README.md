# SugarClient 1.21.11

A modular Minecraft Java client mod built with Fabric and Java 21.

## Project status

- Target Minecraft: 1.21.11
- Loader: Fabric
- Java: 21
- Main package: `dev.sugarexploit.client`
- Mod ID: `sugarexploit_client`

This repository is being implemented in small, verifiable stages. The first milestone is a clean client entrypoint, module lifecycle, typed settings, and a basic in-game interface. Gameplay modules will be added only after the base project builds and loads reliably.

## Architecture

- `module`: Module base class, categories, and module registry.
- `setting`: Typed settings and configuration support.
- `module.impl`: Individual modules, grouped by feature.
- `ui`: Click GUI and HUD components.
- Fabric client events: lifecycle and tick integration.

## Build

The project uses Gradle with Fabric Loom. Once the Gradle wrapper and build files are added, build with:

```sh
./gradlew build
```

The mod JAR will be generated in `build/libs/`.

## Implementation notes

The supplied SugarClient architecture specification is the design reference. The initial milestone focuses on the framework foundation; the complete module catalog is a larger follow-up task and is not represented as finished yet.
