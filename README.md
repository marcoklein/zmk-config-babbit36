# zmk-config-babbit36

ZMK firmware config for the **Babbit36** keyboard (XIAO BLE + 74HC595 shift register, 36-key split).

## Keymap

```
╭───────────┬──────────┬──────────┬──────────┬──────────╮   ╭──────────┬──────────┬──────────┬──────────┬──────────╮
     Q          W          F          P          B              J          L          U          Y          ;
├───────────┼──────────┼──────────┼──────────┼──────────┤   ├──────────┼──────────┼──────────┼──────────┼──────────┤
   LGUI A     LALT R    LCTRL S    LSHFT T       G              M       RSHFT N    RCTRL E    RALT I     RGUI O
├───────────┼──────────┼──────────┼──────────┼──────────┤   ├──────────┼──────────┼──────────┼──────────┼──────────┤
     Z          X          C          D          V              K          H          ,          .          /
╰───────────┴──────────┼──────────┼──────────┼──────────┤   ├──────────┼──────────┼──────────┴──────────┴──────────╯
                   NAV/ESC   LOWER/TAB   RAISE/BSPC        RAISE/RET   LOWER/SPC       DEL
                   ╰─────────┴──────────┴──────────╯   ╰──────────┴──────────┴──────────╯
```

### Layers

| Layer | Hold key | Content |
|-------|----------|---------|
| **RAISE** | BSPC or RET | Numbers 1-0, arrows, DEL, grave, brackets, PG_UP/DN |
| **LOWER** | TAB or SPC | Symbols (!@#$%^&* etc.), `'`, `"`, pipe |
| **NAV** | ESC | Bluetooth profiles (Q-P), clear pairings (A), bootloader (G), sys_reset (P), arrows, printscreen |

### Homerow mods

| Key | Mod |
|-----|-----|
| A | LGUI |
| R | LALT |
| S | LCTRL |
| T | LSHIFT |
| N | RSHIFT |
| E | RCTRL |
| I | RALT |
| O | RGUI |

## Build

Pushes to `main` trigger GitHub Actions. Download firmware from the latest [Actions run](https://github.com/marcoklein/zmk-config-babbit36/actions).

## Flash

1. Connect XIAO BLE via USB-C
2. Double-tap reset button → `XIAO-SENSE` drive mounts
3. Drag `.uf2` file onto the drive
4. Keyboard reboots automatically
