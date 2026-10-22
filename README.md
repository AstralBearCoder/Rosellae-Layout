<div align="center">
<h1>Rosellæ</h1>
 
<h3>A trilingual keyboard layout for French · English · Spanish</h3>
<h4>Runs on `United States International` system layout</h4>
 
<h2>
  👉 <a href="https://astralbearcoder.github.io/Rosellae-Layout/">OPEN THE INTERACTIVE LAYOUT VIEWER</a> 👈
</h2>
<p><em>See every layer, every key and every finger color live, no install needed.</em></p>
<img src="Screen/7" alt="Rosellae, Base 30-key letter layout" width="100%">
</div>
---
 
## ⚡ Quick start
 
| I have… | Go to | Time |
|---|---|---|
| A **Piantor BT** (42-key split, ZMK) | [Piantor setup](#-piantor-bt-zmk) | ~5 min |
| A **normal ISO keyboard** on **Windows** (laptop or desktop) | [Kanata setup](#-classic-iso-keyboard-kanata-windows) | ~2 min |
| Any other 30+ key keyboard | Use the [viewer](https://astralbearcoder.github.io/Rosellae-Layout/) as a reference and adapt the layout | n/a |
 
---
 
## ✨ Why Rosellæ?
 
- **One alpha layer for three languages.** No switching, no compromise between French, English and Spanish.
- **All accents on one sticky layer (`★`).** `é è à ù ç œ æ` · `ñ á í ó ú` · `ä ö ü`: press `★` once, then the letter. The base layer stays clean and fast.
- **Left-hand shortcuts on the `★` layer.** Undo, Redo, Cut, Copy, Paste, Select all (`^z ^y ^x ^c ^v ^a`) so your right hand can stay on the mouse.
- **`QU` macro.** `Q` types `qu` (it is followed by `u` almost every time in all three languages). A solo `q` lives on the `★` layer.
- **Smart paired brackets** `[ { ( ) } ]`. Typing the opening one inserts the closing one and puts the cursor inside, like in most IDEs.
- **Paired Spanish punctuation** `¿?` and `¡!`. Same principle: both signs are typed and the cursor lands between them.
> **A-Rosellae (Astral-Rosellae)** is my personal application of Rosellæ, built on the `United States International` system layout so that accents work natively without Unicode. You are free to adapt it or build your own system on top of the Rosellæ alpha layer.
 
---
 
## 🎹 Piantor BT (ZMK)
 
**42-key split keyboard, 6-key thumb cluster.** Uses dedicated keys, sticky modifiers and hardware combos. No home row mods.
 
![Rosellæ on the Piantor, with all layers](Screen/8)
 
### Files (folder [`Piantor 42-keys | ZMK Configuration`](<./Piantor%2042-keys%20%7C%20ZMK%20Configuration>))
 
| File | Role |
|---|---|
| `piantor_left.uf2` | Layout for the **left** half |
| `piantor_right.uf2` | Layout for the **right** half |
| `settings_reset-piantor_pro_bt_left-zmk.uf2` | **Reset** for the left half |
| `settings_reset-piantor_pro_bt_right-zmk.uf2` | **Reset** for the right half |
 
### Install
 
> 💡 Do this for **each half**, one at a time. First time, or if anything behaves strangely, start with the reset (step 2).
 
1. **Download** the folder (green **Code** button → *Download ZIP*, or grab it from [Releases](../../releases)) and unzip it.
2. **Reset (recommended first time):**
   1. Plug the half in via USB.
   2. **Double-tap the reset button** on the Nice!Nano. A drive named `NICENANO` appears.
   3. Drag and drop the matching `settings_reset-…_left` / `_right` `.uf2` file onto it. The drive closes by itself.
3. **Flash the layout:**
   1. Double-tap reset again, `NICENANO` reappears.
   2. Drag and drop `piantor_left.uf2` (left half) or `piantor_right.uf2` (right half).
4. Repeat for the other half. Done ✅
### Customize
 
Compatible with [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/): connect it to your fork of this repo, edit keys, sticky layers or combos visually, and commit. GitHub Actions rebuilds the `.uf2` files automatically (Actions tab → latest run → Artifacts).
 
---
 
## ⌨️ Classic ISO keyboard (Kanata, Windows)
 
**Any standard ISO keyboard**, no custom hardware needed. Remapping is done in software by [Kanata](https://github.com/jtroo/kanata).
 
![Rosellæ on ISO Classic, with all layers](Screen/9)
 
### Files (folder [`Classic ISO min 39-keys | Kanata Configuration`](<./Classic%20ISO%20min%2039-keys%20%7C%20Kanata%20Configuration>))
 
| File | Role |
|---|---|
| `Rosellae_Driver.bat` | **Double-click this.** Starts Kanata with the layout |
| `Master.kbd` | The layout configuration (timings, layers, accents) |
| `kanata_windows_gui_winIOv2_x64.exe` | Kanata itself (the engine) |
 
### Install
 
1. **Download** the folder (green **Code** button → *Download ZIP*, or from [Releases](../../releases)) and unzip it.
2. **Keep the 3 files together** in the same folder.
3. **Double-click `Rosellae_Driver.bat`.** Rosellæ is now active.
4. If Windows shows a *SmartScreen* warning: click **More info → Run anyway**.
**To stop it:** close the Kanata window (or its tray icon).
 
### Start automatically with Windows (optional)
 
1. Right-click `Rosellae_Driver.bat` → **Create shortcut**.
2. Press `Win + R`, type `shell:startup`, press Enter.
3. Move the shortcut into the folder that opens.
### Customize
 
Open `Master.kbd` in any text editor, change what you want, save, then restart `Rosellae_Driver.bat`.
 
---
 
## 🙌 Credits
 
Created by [AstralBearCoder](https://github.com/AstralBearCoder). Powered by [ZMK](https://zmk.dev/) and [Kanata](https://github.com/jtroo/kanata).
 
