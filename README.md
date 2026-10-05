# Rosellae

A keyboard layout for the **Piantor BT** (ZMK) and for standard keyboards
via **Kanata**. [One sentence on the idea: e.g. "Designed for typing in
English and X, built around home row mods and a small number of layers."]

![Layout](images/layout.png)

## Overview

- **Layers:** [number and names, e.g. Base, Nav, Num, Sym]
- **Home row mods:** [yes/no, and which]
- **Languages / special characters:** [if relevant]

## Repository layout

| Path | What it is |
|------|------------|
| `config/` | ZMK config for the Piantor BT (edited with Keymap Editor) |
| `build.yaml` | ZMK firmware build targets |
| `kanata/` | Kanata configs for use on a PC |
| `images/` | Layout diagrams |

## Piantor BT (ZMK)

1. Open the **Actions** tab and download the latest firmware artifact.
2. Flash the `.uf2` files to the left and right halves.
3. To edit the layout, use [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)
   and connect it to this repo.

## Kanata

The Kanata configs mirror the Piantor layout as closely as possible.
Because a regular keyboard has fewer keys, some things differ:

| Piantor feature | Kanata equivalent |
|-----------------|-------------------|
| [e.g. thumb keys] | [e.g. mapped to Space/Alt/etc.] |
| [e.g. dedicated Nav layer key] | [e.g. held CapsLock] |
| [e.g. key X] | [not available] |

Run it with:

    kanata --cfg kanata/rosellae-laptop.kbd

See [`kanata/README.md`](kanata/README.md) for platform notes.

## License

MIT
