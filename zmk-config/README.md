# Helix ZMK Config (Split 25+25)

This is a starter `zmk-config` for a split Helix-style keyboard with 25 keys per half.

It builds two artifacts:
- `helix-left.uf2`
- `helix-right.uf2`

## What is included

- Base text layer (letters and common modifiers)
- Numbers/symbols layer (momentary)
- macOS actions layer (momentary), including `&bootloader`

## Important

`build.yaml` uses:
- `board: nrfmicro_13`
- `shield: helix_left` / `helix_right`

If your shield or board names differ in your firmware source, update those values in `build.yaml`.

## Build via GitHub Actions

1. Push this folder content to a dedicated `zmk-config` repository.
2. Run the `Build ZMK Firmware` workflow.
3. Download artifacts and flash:
   - left half with `helix-left.uf2`
   - right half with `helix-right.uf2`

## Flash flow

1. Enter bootloader on each half.
2. Mount `NRF52BOOT`.
3. Copy corresponding `.uf2`.
4. Wait for auto-reboot.
