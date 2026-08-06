<div align="center">

# HyCreator

**A desktop editor for Hytale server assets. Windows & Linux.**

Stop hand-editing raw JSON. Real forms built from the game's own schemas, live 3D previews, engine-exact simulators, and one-click deploy to your game.

[![Latest release](https://img.shields.io/github/v/release/lewai1/HyCreator-releases?label=download&color=2ea44f)](https://github.com/lewai1/HyCreator-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/lewai1/HyCreator-releases/total?color=8250df)](https://github.com/lewai1/HyCreator-releases/releases)
[![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20Linux-1f6feb)](#download)
[![Discord](https://img.shields.io/badge/Discord-join%20the%20server-5865F2?logo=discord&logoColor=white)](https://discord.gg/7kbpXhSRrV)

</div>

---

## Download

Grab the latest build from the **[Releases page](https://github.com/lewai1/HyCreator-releases/releases/latest)**.

| Platform | File | Notes |
| --- | --- | --- |
| Windows 10 / 11 | `HyCreator.exe` | Portable, no installer. Drop it anywhere and run. |
| Linux (Debian / Ubuntu) | `HyCreator_x.y.z_amd64.deb` | `sudo apt install ./HyCreator_x.y.z_amd64.deb` |
| Linux (any distro) | `HyCreator_x.y.z.AppImage` | `chmod +x` then run. |

HyCreator checks for updates on launch and offers new releases as they ship.

> **Windows SmartScreen / Defender may flag the first run.** That is the normal fate of a brand-new, unsigned program Windows has never seen before: a false positive that fades as the app builds reputation. If it happens, click *More info*, then *Run anyway*.

**Requirements.** Windows needs the WebView2 runtime, preinstalled on Windows 11 and up-to-date Windows 10 (otherwise [get it here](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)). Linux needs a reasonably current distro: the `.deb` declares its dependencies (WebKitGTK 4.1), and the AppImage carries most of what it needs.

## Getting started

1. Launch HyCreator and open a workspace: your **game install** (it finds `Assets.zip` on its own), the **Shared Source** (the `HytaleAssets` folder Hypixel provides to shared source members, [request access here](https://accounts.hytale.com/shared-source)), or a **mod folder**.
2. Open any file. Roles, items, blocks, recipes, droplists, effects, particles, prefabs, worldgen, translations, custom UI: everything gets an editor, and mods resolve every vanilla asset they reference but don't ship.
3. Edit in real forms, watch the previews, hit Ctrl+S. Saves are byte-exact, so your git diffs only show what *you* changed.

## What it does

**Forms, not JSON.** Every field is typed from the game's own schemas, with documentation on hover, autocomplete everywhere an id goes, enum dropdowns, reference browsing, and validation that points at the exact broken field. Nothing is hardcoded: a new Hytale version drops, the editor follows.

**You see what you edit.** Models and NPCs render in 3D with their gear and animations. Items bake their icons exactly like the game does. Particles, prefabs, weathers and status effects preview live; a status effect plays its model VFX *and* its particle systems together, the way the game applies it. Sound references get a play button.

**Dedicated editors where JSON hurts most.** Droplists show live drop chances on every entry and simulate rolls with the engine's exact algorithm. Recipes display their real crafting layout. NPC brains render as node graphs: sensors, actions, states, the whole decision tree. Weapon movesets chart as combo graphs you can edit from. CAE curves are plotted, with a scorer that ranks actions the way the engine would. MobStudio previews attack selectors and hitboxes on the actual mob.

**Refactoring that follows references.** Rename an asset and every reference in your mod follows. Fork any vanilla asset *with its whole dependency chain*. Diff your files against the vanilla they shadow. Scan a mod for broken references and deprecated fields before your server finds them. An unused-asset report helps when you want to clean up.

**Patch support.** [Patchly](https://www.curseforge.com/hytale/mods/patchly) `.patch`/`.put` files and [Patchwork](https://www.curseforge.com/hytale/mods/patchwork) definitions are first-class: form editing, live merge preview against the resolved target, and variables evaluated with the runtime's own semantics.

**Java plugins.** Build your mod's Gradle project from the app (Ctrl+B), with compiler errors as clickable chips. New projects scaffold from [AzureDoom's mod template](https://template.azuredoom.com/). The Java editor completes against the exact server jar your project compiles against, fully offline, and an API browser puts the whole server API and its javadoc one shortcut away.

**Server Link.** Mirror a live server over SFTP or the Pterodactyl panel, edit locally, and let your saves upload automatically, with remote changes polled back in.

**Quality of life.** Quick open (Ctrl+P), find in files, a command palette for every action, split view, detachable windows, dark/light/OLED and fully custom themes, local edit history with one-click revert, automatic backups and crash drafts.

## Community field descriptions

Hytale's own schemas document a lot, but thousands of asset fields ship with no description at all. **[hytale-field-descriptions](https://github.com/lewai1/hytale-field-descriptions)** is the community answer: plain-text explanations, written by the people who figured a field out, that HyCreator shows as tooltips.

Two rules keep it trustworthy. Official documentation **always wins**, so a community entry only ever fills a field that has none. And community text is always labelled as community in the tooltip, so crowd knowledge never passes as official.

- **Get them:** they ship with each release, and *Settings → Community field descriptions → ⟳ Update* pulls the latest without waiting for a new build.
- **Contribute one:** right-click any undocumented field in the editor and pick **✎ Suggest a description**. It opens a pre-filled GitHub issue naming the field and where you saw it; you write what it does and how you verified it.

If you have spent an evening working out what a field really controls, that hour is worth sharing. Every accepted description becomes a tooltip for everyone.

## Source code

This repository hosts the release builds. The source code repository will be published soon.

## Community & feedback

Questions, bug reports, ideas: the fastest lane is the **[Discord server](https://discord.gg/7kbpXhSRrV)**. Issues opened on this repository are read too.

## Credits

Thanks to **[DemoHytale](https://x.com/DemoHytale)** for the HyCreator name and **[Starky_TV](https://x.com/Starky_TV)** for the icon, and to everyone testing builds and filing the field reports that shaped almost every feature in here.

---

*HyCreator is an unofficial community tool. It is not affiliated with, endorsed by, or supported by Hypixel Studios. Hytale and all related assets are the property of their respective owners.*
