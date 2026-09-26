# MA3 Mods

Mods for the native grandMA3 user interface, installed and removed from the console with the **MA3 Mods** plugin
(Tensegrity Lighting Service — Florian Declercq).

> **Status: tested on grandMA3 onPC only — not yet tested on console hardware.**

This repository is the update source of the plugin:

| File | Purpose |
|---|---|
| `catalog.lua` | published mods (version, size, checksum) and plugin version |
| `packages/*.ma3mod` | mod packages, **encrypted**: readable only with the MA3 Mods password |
| `plugin/MA3Mods.xml` | the MA3 Mods plugin (engine only, no mods) to import into the show |
| `MA3Mods-USB-key.zip` | **ready to share**: the plugin inside the USB key folder structure (`grandMA3/…/FDPlugins/MA3Mods/`) + quick guide |

## Quick start
Unzip `MA3Mods-USB-key.zip` at the root of a USB key, import `MA3Mods.xml` into the show, then use
"Update (Internet)" (password) and switch the mods on. The plugin can also prepare an empty USB key by itself
("USB key" drop-down): it creates the folder and copies itself there, ready to import.

## Mods
| Mod | What it does |
|---|---|
| MAtricks Easy Offset (onPC only) | Adds Delay Offset and Phase Offset sliders under From/To (X, Y, Z) in every MAtricks editor: swipe to shift From and To together. |
| Recipe Edit Selection Fix (onPC only) | Sequence Sheet recipe area: the tool button "Edit selection" opens every recipe selected with the lasso, instead of only the last cell. |
| Special Dialog Tools (onPC only) | Shaper and Color special dialogs: a Resolution button next to View / Control / Link (Color Space) makes the dialog encoders finer — Coarse ×1, Fine ×0.1, Increment ×0.01, remembered per user and per dialog. Shaper: Mirror 1/3, Mirror 2/4 and Mirror Rot buttons in the encoder bar (the native Mirror Bar functions, hidden by default). |

## How it works
- The plugin contains no mod; mods live on a USB key (`FDPlugins/MA3Mods/`).
- Mods are applied as small blocks in the MA interface files, each preceded by a marker that holds the original
  lines: switching a mod off and "Restore console" always work, even without the key, and changes made by other
  plugins are preserved.
- Updates are manual (button), password-protected, and only contact GitHub when the station has Internet access
  (curl or wget).
- MA must be restarted after each change.

Validated MA versions (onPC): 2.5.0.3, 2.5.1.0.
