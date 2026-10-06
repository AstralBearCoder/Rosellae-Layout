# Rosellæ

**An optimized keyboard layout, 50/50 French & English, Spanish compatible.**

## Rosellae, Base layout, layout by GalileoBlue (goat)

The alpha core, 3 rows of 5 keys per hand (30-keys total)
The colors show which finger types each key (red: pinky, orange: ring, green: middle, blue: index).


![Rosellae, Base 30-key letter layout](images/TheImage)

## Rosellae - Version Astral

Rosellae - Version Astral is my personal aplication of the rosellae layout, it is designed to work on:
 - **Piantor BT** (ZMK)
 - **Any Classic ISO keyboard**.

This is my personal application, your are free to adapt it or create a completely different system to go with the rosellae layout.

👉 **[Interactive layout viewer]([https://astralbearcoder.github.io/Rosellae-Layout/])**

![Rosellæ on the Piantor, with all layers](images/piantor-layout.png)


### Highlights

- **Three languages:** tuned for French and English, with full Spanish support (`ñ`, `¿?`, `¡!`, accented vowels).
- **One-shot layers** for accents and symbols, so no chords and no held keys for accented letters.
- **Home row mods** for Win / Ctrl / Alt on both hands.
- **Dedicated `QU` key** and `æ` / `œ` for French.
- **Combos** on the Piantor for shutdown, screenshots and the word "où".
- **Two geometries**, one layout: Piantor (ZMK) and Classic ISO (Kanata).

### Layout statistics

| Language | Corpus | SBS | SFS |
|----------|--------|-----|-----|
| French | `lexique4_5K` | 0.81% | 4.84% |
| English | `en_5K` list | 1.00% | 5.34% |
| Spanish | `es_5K` list | 1.03% | 5.80% |

### The base layer

Shifted punctuation: `'` → `"`, `,` → `?`, `.` → `!`, `:` → `;`.

### Piantor thumb and outer keys

| | Left hand | Right hand |
|---|---|---|
| **Outer column** (top to bottom) | Esc, Tab, Win | Backspace, Enter, Ctrl+Shift |
| **Thumbs** | Shift, ★ Accents, Ctrl | Nav, Space, AltGr |

On each hand, the thumbs are listed from the outside toward the center of the keyboard.

### Home row mods (hold)

| Left hand | R | T | S |
|---|---|---|---|
| Hold | Win | Ctrl | Alt |

| Right hand | H | E | I |
|---|---|---|---|
| Hold | Alt | Ctrl | Win |

## Layers

The four layers of the Piantor version: Alpha, Accents (★), Symbols (AltGr) and Navigation (Nav).

![The four layers of Rosellæ on the Piantor](images/layers.png)

### 1. Alpha layer
The base layer shown above.

### 2. Accents layer (★), one-shot
Tap ★, then the letter. Gives all the French and Spanish accents on the same key as the base letter:

`é è ê ë` · `à â ä` · `ù û ü` · `î ï` · `ô ö` · `œ æ` · `ç` · `ñ` · `á í ó ú`

It also holds the clipboard shortcuts on the left hand: `Ctrl+Z` (undo), `Ctrl+Y` (redo), `Ctrl+X`, `Ctrl+C`, `Ctrl+V`, `Ctrl+A`.

### 3. Symbols layer (AltGr), one-shot
Tap AltGr, then the symbol. Pairs such as `[]` `()` `{}` close automatically and return the cursor between them. Includes `€ $ ^ * ~ ` + = - _ < > & @ # % | \ /`, `×`, `→`, and the Spanish `¿?` and `¡!`.

### 4. Navigation layer (Nav), momentary
Hold Nav (hold Space on the ISO version). Gives:

- Arrow keys on the home row (`n ← · r ↓ · t ↑ · s →`)
- Media controls (previous, play/pause, next)
- Page up / page down and the two end-of-line / start-of-line keys
- A number block (`0`–`9`) with `,` `.` `/` `=` `%`
- Function keys `F2`, `F4`, `F11`

## Combos (Piantor)

Keys pressed at the same time:

![Rosellæ combos: Power, ScreenShot and Où](images/combos.png)

| Combo | Keys pressed together | Result |
|-------|-----------------------|--------|
| **Power** | The 3 right thumb keys (Nav + Space + AltGr) | `Alt + F4` (closes the active window or opens shutdown) |
| **ScreenShot** | Both inner thumbs (Ctrl + Nav) | `Win + Shift + S` (screen snip) |
| **Où** | `'` + `O` + `U` | Types `où ` followed by a space |

## Classic ISO version (Kanata)

For standard keyboards, the same layout fits in a **minimum of 39 keys**. The keys marked × in the diagram are unused and left untouched.

![Rosellæ on a Classic ISO keyboard](images/iso-layout.png)

Differences from the Piantor:

- There are no dedicated thumb keys, so **Nav is reached by holding Space**.
- ★ Accents, Shift and AltGr sit on the bottom row.
- An **On/Off** key in the top-left corner toggles the remapping.
- Combos are only available on the Piantor.

## Repository contents

| Path | Description |
|------|-------------|
| `config/` | ZMK configuration for the Piantor BT (edited with [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)) |
| `build.yaml` | ZMK firmware build targets |
| `kanata/` | Kanata configuration for the Classic ISO version |
| `docs/` | Interactive layout viewer (`index.html`), published with GitHub Pages |
| `images/` | Layout diagrams and photos used in this README |

## Installation

### Piantor BT (ZMK)

1. Open the **Actions** tab of this repository and open the latest successful build.
2. Download the firmware from the **Artifacts** section.
3. Flash the `.uf2` file to the left half, then the right half.

To modify the layout, connect Keymap Editor to this repository, make your changes, and commit. GitHub builds the new firmware automatically.

### Classic ISO (Kanata)

1. Install [Kanata](https://github.com/jtroo/kanata) for your operating system.
2. Run it with the config from this repository:

```
kanata --cfg kanata/rosellae.kbd
```

## License

MIT
