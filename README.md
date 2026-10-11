# PojavLauncher iOS — Minecraft Java Edition Without JIT

**PojavLauncher No JIT by AppleJR** is a community project for playing Minecraft Java Edition on iPhone and iPad using an interpreter runtime. Development focuses on practical game settings, terrain loading, and compatibility with newer iOS versions.

**[Download PojavLauncher for iOS and view the installation guide](https://applejr.net/pojavlauncher/)**

The AppleJR project page is the main destination for IPA downloads, installation information, and build updates. This repository provides documentation and a starting point for choosing your Minecraft version and settings.

## What is PojavLauncher No JIT?

PojavLauncher brings Minecraft Java Edition to mobile devices. The AppleJR edition builds on the PojavLauncher and Amethyst ecosystem, with a precompiled Java interpreter that can launch supported game profiles without enabling Just-In-Time compilation.

The project aims to make Java Edition more accessible through sideloading, with conservative memory settings and performance work for compatible game versions. Java Edition remains demanding: loading times and frame rates depend on the Minecraft version, world, mods, device, and available memory.

## Minecraft versions and starting settings

| Minecraft version | Suggested use | Starting configuration |
| --- | --- | --- |
| Vanilla 1.12.2 | Start here; reported playable by the project tester | Renderer Auto, RAM Auto, Fast graphics |
| Vanilla 1.15.2 | First newer version to evaluate | Start without mods or custom JVM flags |
| Vanilla 1.16.5 | Additional compatibility and performance target | Test Vanilla before trying a mod loader |

Start with a render distance of **4–6 chunks**, a **30 FPS limit**, mipmaps at **0**, clouds off, and the default resource pack. Adjust the view distance after checking how your world runs. These are starting settings, rather than measured performance guarantees.

Use **RAM Auto** initially. It leaves room for native rendering and other app memory; a larger Java heap does not automatically make an interpreted game faster.

## How to install on iPhone or iPad

1. Open the [AppleJR PojavLauncher download page](https://applejr.net/pojavlauncher/) and choose the available build.
2. Follow the installation instructions for your signing method. An IPA must be signed with valid credentials before it can be installed.
3. Open the launcher and sign in with an account that owns Minecraft Java Edition.
4. Select Vanilla **1.12.2**, Renderer **Auto**, and RAM **Auto** for the first test.
5. Enter a world and test movement, touch controls, and loading before trying a newer version.

When updating an existing installation, preserve your launcher data and worlds. Follow the current build notes on the project page if they specify a different configuration.

## Compatibility and development status

iOS **18** and **26**, and iPhone **14 Pro and later**, are development targets. Compatibility must be checked for the specific build, iOS version, and signing method. Newer hardware alone does not guarantee smooth gameplay without JIT.

Recent development has focused on reducing spawn preparation work, optional native terrain calculations for selected Vanilla versions, and deferring unnecessary startup work while keeping data conversion available. Coverage varies by build; experimental changes need on-device validation.

## Frequently asked questions

### Does this edition require JIT?

The AppleJR No JIT edition uses an interpreter runtime for supported profiles. Other PojavLauncher or Amethyst builds may have different runtime and JIT requirements.

### Is this Minecraft Java or Bedrock Edition?

This project concerns **Minecraft Java Edition**. A Minecraft Java Edition license is required to play the game.

### Why does Building terrain take a long time?

Minecraft prepares and loads chunks before entering a world. Generating a new world usually requires more work than reopening an existing one. Lower view distance, default resources, and fewer mods reduce the amount of work the game has to perform.

### Can I use Fabric, Forge, or modpacks?

Support depends on the game version, loader, renderer, and individual mods. Establish a working Vanilla profile first, then test a small set of compatible mods. A working Vanilla profile does not guarantee that a modpack will run well.

### What should I include in a bug report?

Include the launcher build, device model, iOS version, Minecraft version, renderer, RAM setting, and whether the issue occurs in a new or existing world. Add the latest game log and an iOS crash report when available.

### Where can I get updates and help?

Visit the [PojavLauncher project page on AppleJR](https://applejr.net/pojavlauncher/) for available downloads and instructions, or join the [AppleJR Discord community](https://discord.gg/e58k5bkja3).

## Credits

- **AppleJR** — community project development, testing coordination, and documentation.
- **[PojavLauncher](https://github.com/PojavLauncherTeam/PojavLauncher_iOS)** — the original iOS launcher project.
- **[Amethyst](https://github.com/AngelAuraMC/Amethyst-iOS)** — the launcher ecosystem used by this project.
- **[OpenJDK](https://openjdk.org/)** — Java runtime technology.

Minecraft is developed by Mojang Studios. This community project is not affiliated with Mojang Studios or Microsoft. Upstream projects and dependencies retain their respective licenses.
