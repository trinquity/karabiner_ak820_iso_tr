# Karabiner-Elements Rules for AK820 (ISO) on macOS — TR Layout Fix

This repository contains **Karabiner-Elements Complex Modifications** designed specifically for the **AK820 keyboard (ISO variants)** on macOS, targeting the common character mapping issues experienced when using the **Turkish (TR) keyboard layout**.

The rules are **device-scoped** (Vendor ID `3141`) and support multiple Product IDs (`65278`, `32777`) to cover different AK820 modes/firmware variants.

---

## What This Fixes

AK820 ISO keyboards often behave inconsistently on macOS with TR layout — especially for keys like:

- **Grave / Tilde key** (`grave_accent_and_tilde`)
- **Hyphen key** (`hyphen`)

These JSON rules remap those keys in a way that makes them behave more naturally under TR layout, without affecting other keyboards connected to the system.

---

## Included Rules

### 1) TILDE Remaps (invert ISO - TR)

A full modifier-aware remap for the **grave/tilde key**, handling:

- Normal press
- Shift press
- Option press

This version is intended for the “inverted ISO” behavior where the key produces unexpected characters depending on modifiers.

---

### 2) TILDE Remaps (default)

A simpler alternative that:

- Keeps Option behavior intact
- Remaps the base key to a stable output

Useful if you want a minimal fix without full modifier inversion.

---

### 3) HYPHEN Remaps (invert ISO - TR)

A modifier-based remap for the hyphen key to ensure consistent output between:

- Normal hyphen
- Shift-hyphen behavior

Designed to eliminate the common TR-layout mismatch where Shift output becomes incorrect on AK820 ISO firmware.

---

## Notes

- These rules are intentionally limited to the AK820 device IDs to avoid impacting other keyboards.
- Output depends on your active macOS input source (intended for Turkish layout).
- If your AK820 reports a different Product ID, you can add it under the same `identifiers` array.
