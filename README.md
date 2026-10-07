# Rosellæ

**An optimized keyboard layout, optimised for typing in French, English & Spanish.**

### 👉 **[Interactive layout viewer](https://astralbearcoder.github.io/Rosellae-Layout/)**


## Alpha Layer 
_The colors show which finger types each key (red: pinky, orange: ring, green: middle, blue: index)._

![Rosellae, Base 30-key letter layout](Screen/6)


## Rosellae - Version Astral

**Rosellae - Version Astral** is my personal application of the Rosellæ layout, featuring custom accent, symbol, and navigation layers. 

It is designed to work on:
- **Piantor BT** (ZMK firmware)

![Rosellæ on the Piantor, with all layers](Screen/2)

- **Any Classic ISO keyboard** (Kanata software remapper)

![Rosellæ on ISO Classic, with all layers](Screen/3)

This is my personal application; you are free to adapt it or create a completely different system to go with the Rosellæ layout.

---

# 1. Rosellæ on Piantor BT (ZMK) — 42-Key Split (6 Thumb Keys)

This version is designed specifically for a 42-key split layout with a 6-key thumb cluster. The configuration files target the **Piantor BT**. It relies entirely on dedicated physical keys, sticky modifiers, and hardware combos—**no home row mods are used here**.

![Rosellæ on the Piantor, with all layers](Screen/2)

---

### 🕹️ Features & Ergonomics

#### 1. The 6-Key Thumb Cluster & Outer Columns
Every modifier and layer switch has its own dedicated physical key:

| Hand | Outer Column (Top to Bottom) | Thumb Cluster (Outer → Inner) |
|---|---|---|
| **Left** | `Esc` · `Tab` · `Win` | `Sticky Shift` · `Sticky ★ Accents` · `Ctrl` |
| **Right** | `Backspace` · `Enter` · `Ctrl+Shift` | `Sticky Nav` · `Space` · `Sticky Symbols (Tap-Dance)` |

#### 2. Advanced Thumb Behaviors
- **Sticky Shift & Sticky Accents:** Both operate as one-shot layers. Tapping `Shift` then `★ Accents` allows you to effortlessly produce uppercase accented letters (`É`, `À`, `Ç`, etc.) without holding any key down.
- **Sticky Symbols + Tap-Dance:**
  - **Single tap or hold:** One-shot switch to the **Symbols** layer.
  - **Double tap (fast succession):** Becomes **Left Alt**, giving you instant access to standard Alt shortcuts.
- **Sticky Navigation:** Tap to enter navigation mode for your next keystroke without locking your thumb down.

#### 3. Mouse-Friendly Left Hand (Accent Layer)
On the **★ Accents Layer**, the left hand contains essential system shortcuts:
- `Ctrl+Z` (Undo), `Ctrl+Y` (Redo), `Ctrl+A` (Select All)
- `Ctrl+X` (Cut), `Ctrl+C` (Copy), `Ctrl+V` (Paste)

> 💡 **Ergonomic Purpose:** You can execute frequent text editing and clipboard operations entirely with your left hand while keeping your **right hand continuously on your mouse**.

#### 4. Smart Typing Features
- **Auto-Closing Delimiters:** Typing `()`, `[]`, or `{}` outputs the pair and automatically places the cursor in the middle.
- **Spanish Punctuation:** `¿?` and `¡!` are typed in a single stroke with the cursor placed between them.
- **Dedicated QU Keys:** Includes automatic macros for `qu`, `Qu`, and `QU`.

#### 5. Hardware Combos
Actions triggered by pressing multiple keys simultaneously:

| Combo | Keys Pressed Together | Result |
|---|---|---|
| **Power / Exit** | All 3 Right Thumb Keys (`Nav` + `Space` + `Symbol`) | `Alt + F4` (Closes window / prompts shutdown) |
| **Screenshot** | Both Inner Thumbs (`Ctrl` + `Nav`) | `Win + Shift + S` (Snipping tool) |
| **Word "où"** | `'` + `O` + `U` | Types `où ` with a trailing space |

---

### 💾 Installation & Flashing (Piantor BT)

1. **Download the Firmware:**
   - Go to the **Actions** tab of this repository.
   - Click the latest workflow run and download the `.zip` archive from the **Artifacts** section.
2. **Flash Left Half:**
   - Connect the left half via USB.
   - Double-tap the reset button on the Nice!Nano controller. A storage drive named `NICENANO` will appear.
   - Drag and drop `piantor_left.uf2` onto it.
3. **Flash Right Half:**
   - Repeat the exact same operation with the right half using `piantor_right.uf2`.

### ✏️ Customization
This configuration is fully compatible with [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/):
1. Connect Keymap Editor to this GitHub repository.
2. Edit your keys, sticky layers, or combos visually.
3. Commit your changes: GitHub Actions will recompile the `.uf2` files automatically.

---
---

# 2. Rosellæ on Classic ISO Keyboard (Kanata)

This version brings the complete Rosellæ experience to **any standard physical ISO keyboard** (laptop or desktop) without custom hardware, using the high-performance remapper [Kanata](https://github.com/jtroo/kanata).

![Rosellæ on ISO Classic, with all layers](Screen/3)

---

### 🕹️ Features & Ergonomics

#### 1. Angle Mod (Physical Ergonomics)
On traditional row-staggered keyboards, the bottom-left row forces the left wrist into an uncomfortable inward bend (*ulnar deviation*).  
Rosellæ implements an **Angle Mod**, which shifts the entire bottom-left row **one key to the left** (using the ISO `<` key next to Shift):
- Your left hand rests in a natural, straight posture, mirroring the natural column alignment of ergonomic keyboards.
- The layout isolates a compact **39-key core zone**; all outer keys marked with `×` in diagrams are ignored.

#### 2. Home Row Mods (HRM)
Since standard keyboards only have a single physical spacebar and lack split thumb clusters, modifiers are placed directly on the home row letters:

| Left Hand | R | T | S | | Right Hand | H | E | I |
|:---|:---:|:---:|:---:|---|:---|:---:|:---:|:---:|
| **Tap** | `r` | `t` | `s` | | **Tap** | `h` | `e` | `i` |
| **Hold** | **Win (LMet)** | **Ctrl (LCtl)** | **Alt (LAlt)** | | **Hold** | **Alt (LAlt)** | **Ctrl (RCtl)** | **Win (RMet)** |

- **How it works:** Tapping a key normally outputs its letter. Holding it down (configured with a reliable 350ms threshold) turns it into a modifier.
- **Why it matters:** You can trigger complex shortcuts (e.g., `Ctrl+Alt+...`) directly from your resting position without contorting your fingers to reach the bottom corners of the keyboard.

#### 3. Space-Cadet Navigation (`@nav`)
With only a single physical spacebar available:
- **Tap Space:** Types a standard space.
- **Hold Space (175ms):** Momentarily reveals the **Navigation Layer**:
  - **Left Hand:** Arrow cluster on the home row (`N` ←, `R` ↓, `T` ↑, `S` →), plus `Home`, `End`, `PgUp`, `PgDn`, and media keys (`Prev`, `Play/Pause`, `Next`).
  - **Right Hand:** Full numpad (`0–9`, `.`, `,`, `/`, `=`, `%`) and function keys (`F2`, `F4`, `F11`).

#### 4. Sticky Layers & Shifted Accents
- **One-Shot Timers:** `★ Accents`, `Shift`, and `Symbols` are configured as one-shot keys with a 1000ms window—tap them once, and the layer stays primed for your next keypress.
- **Shift + Accent Chain (`@sft_acc`):** Tapping `Shift` followed by `★ Accents` automatically enters the dedicated **Uppercase Accents Layer** (`É`, `È`, `À`, `Ç`, `Ñ`, `Œ`, `Æ`, etc.), fully injected as 100% native Unicode characters.
- **Left-Hand Mouse Shortcuts:** Just like the Piantor version, the Accent layer maps `Ctrl+Z`, `Ctrl+Y`, `Ctrl+X`, `Ctrl+C`, `Ctrl+V`, and `Ctrl+A` to the left hand, enabling one-handed edits while using the mouse.

#### 5. Smart Typing Features
- **Auto-Closing Delimiters:** Typing `()`, `[]`, or `{}` outputs the pair and automatically places the cursor in the middle (`left` macro).
- **Spanish Punctuation:** `¿?` and `¡!` are typed in a single stroke with the cursor placed between them.
- **Dedicated QU Keys:** Includes automatic macros for `qu`, `Qu`, and `QU`.
- **Windows AltGr Fix:** Kanata automatically cancels synthetic left-control events (`windows-altgr cancel-lctl-press`), avoiding classic Windows AltGr bugs.

#### 6. Instant Gaming / Raw Toggle
The top-left key (typically `²` or `grv`) acts as a master hardware bypass:
- Press it to switch to the **`off` layer** (standard ISO layout), perfect for gaming or sharing your computer.
- Press it again (`@tobase`) to reactivate Rosellæ.

---

### 💾 Installation & Setup (Kanata)

#### Step 1: Install Kanata
- **Windows:**
  Using winget:
  ```powershell
  winget install jtroo.kanata
  ```
  *(Or download `kanata.exe` directly from the [Kanata Releases page](https://github.com/jtroo/kanata/releases)).*

- **Linux:**
  Download the binary, make it executable, and move it to your system PATH:
  ```bash
  chmod +x kanata
  sudo mv kanata /usr/local/bin/
  ```

- **macOS:**
  Using Homebrew:
  ```bash
  brew install kanata
  ```

#### Step 2: Run Rosellæ
Clone or download this repository, open a terminal in the folder, and run:
```bash
kanata --cfg kanata/rosellae.kbd
```
> **Note for Linux users:** Kanata requires read/write access to `/dev/uinput`. Run with `sudo` or configure appropriate `udev` rules.

#### Step 3: Run Automatically on Boot (Optional)
- **Windows:**
  1. Create a shortcut to `kanata.exe`.
  2. Right-click the shortcut → **Properties** → in the **Target** field, add `-c "C:\path\to\kanata\rosellae.kbd"`.
  3. Press `Win + R`, enter `shell:startup`, and place the shortcut there.
- **Linux:**
  Set up a user systemd service to run Kanata silently in the background on login.

### ✏️ Customization
All timings, Unicode mappings, and aliases are defined inside:
```text
kanata/rosellae.kbd
```
Modify this file with any text editor and restart Kanata to reload your changes.

---
