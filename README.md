<div align="center">

# HyCreator

A desktop editor for Hytale server assets, for Windows and Linux.

[![Latest release](https://img.shields.io/github/v/release/lewai1/HyCreator-releases?label=download&color=2ea44f)](https://github.com/lewai1/HyCreator-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/lewai1/HyCreator-releases/total?color=8250df)](https://github.com/lewai1/HyCreator-releases/releases)
[![Discord](https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white)](https://discord.gg/7kbpXhSRrV)

</div>

## Download

Get the latest build from the [Releases page](https://github.com/lewai1/HyCreator-releases/releases/latest).

| System | File | How to run |
| --- | --- | --- |
| Windows 10 / 11 | `HyCreator.exe` | No installer. Put it anywhere and run it. |
| Debian / Ubuntu | `HyCreator_x.y.z_amd64.deb` | `sudo apt install ./HyCreator_x.y.z_amd64.deb` |
| Fedora / RHEL / openSUSE | `HyCreator-x.y.z-1.x86_64.rpm` | `sudo dnf install ./HyCreator-x.y.z-1.x86_64.rpm` |
| Any Linux | `HyCreator.AppImage` | `chmod +x HyCreator.AppImage`, then run it. |

HyCreator checks for updates when it starts and can install them itself.

Windows needs the WebView2 runtime. It comes with Windows 11 and recent Windows 10, otherwise [download it here](https://developer.microsoft.com/en-us/microsoft-edge/webview2/).

The exe is not code-signed yet, so SmartScreen may warn on the first launch. Click **More info**, then **Run anyway**. You can also check any release file on [VirusTotal](https://www.virustotal.com/gui/home/upload).

## Getting started

1. Open a workspace. It can be your game install (HyCreator finds `Assets.zip`), the [Shared Source](https://accounts.hytale.com/shared-source) `HytaleAssets` folder, a mod folder, or a whole mods folder.
2. Open a file. Roles, items, blocks, recipes, drop lists, particles, prefabs, worldgen, translations and UI files all have an editor. Vanilla assets your mod references are found automatically.
3. Edit, check the preview, save with Ctrl+S. Files are saved exactly as they were written, so a git diff only shows your changes.

## Features

- Forms built from the game's own schemas, with typed fields, documentation on hover, id autocomplete and validation on the exact field.
- 3D previews for models and NPCs with their gear and animations, item icons, particles, prefabs, weathers and status effects.
- Dedicated editors for drop lists (drop chances and roll simulation), recipes, NPC behaviour graphs, weapon combos, combat action curves and ability runes.
- MobStudio, to see an NPC's attacks, hitboxes and timings on the mob itself.
- Renaming an asset updates every reference to it. Vanilla assets can be copied into your mod with everything they depend on.
- Checks for broken references, deprecated fields and unused assets, and a diff against the vanilla files you override.
- A whole mods folder opens in load order and shows which copy of an asset the game keeps.
- [Patchly](https://www.curseforge.com/hytale/mods/patchly) and [Patchwork](https://www.curseforge.com/hytale/mods/patchwork) patch files with a live merge preview.
- Git: review changes, commit, pull, push, branches and tags.
- Java plugins: Gradle build from the app (Ctrl+B), completion against the server jar and a server API browser.
- Server Link: edit a server's files over SFTP or Pterodactyl, saves upload automatically.
- Quick open (Ctrl+P), search in files, command palette, split view, themes, edit history and automatic backups.

## Field descriptions

Many asset fields have no description in the game's schemas. The [hytale-field-descriptions](https://github.com/lewai1/hytale-field-descriptions) repository collects descriptions written by modders, and HyCreator shows them as tooltips, marked as community text. Official documentation always takes priority.

To suggest one, right-click a field without a description and choose **Suggest a description**. It opens a pre-filled GitHub issue.

## Feedback

Questions, bugs and ideas are welcome on the [Discord server](https://discord.gg/7kbpXhSRrV). Issues on this repository are read too.

This repository only hosts the release builds. The source code will be published later.

## Credits

Thanks to [DemoHytale](https://x.com/DemoHytale) for the name, [Starky_TV](https://x.com/Starky_TV) for the icon, and everyone who tests the builds and reports bugs.

---

*HyCreator is an unofficial community tool, not affiliated with or endorsed by Hypixel Studios. Hytale and its assets belong to their respective owners.*
