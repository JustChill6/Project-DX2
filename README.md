<p align="center">
  <img src="./logobanner.png" alt="Project-DX2 Logo" />
</p>

# Project-DX2 — VTech MOD Station (M0D V5: Eclipse)

A lightweight, portable, self-contained Windows desktop modding suite for the **VTech KidiZoom Smartwatch DX2** (`54-193800-A03-000-S00` and regional variants). Designed for safe USB Mass Storage modding—no risky firmware flashing required.

---

## ✨ What's New in Version 5 (Eclipse)

* **Portable Single-EXE Mode:** `VTech MOD Station.exe` embeds the `DATA` asset archive internally and automatically extracts or generates fallback `240×240` assets if run standalone on a new PC.
* **Native 240×240 Auto-Resizer & Live Preview:** Import any `.PNG`, `.JPG`, or `.BMP` image to automatically scale, adjust brightness, and convert to `240×240` baseline JPEGs (`bg.jpg` and `100_0001.jpg`) with side-by-side previewing.
* **Batch Seasonal Theme Generator:** Apply a single master image across all 8 seasonal theme folders at once with optional seasonal color tinting.
* **Watch-Face `.BIN` Validator & Hex Inspector:** Verifies 4-byte alignment and non-zero payload integrity with an interactive hex dump preview before deploying `PCF_0001.BIN`.
* **Auto-Backup & One-Click Restore:** Automatically creates timestamped watch snapshots under `Backups/` before applying mods and supports one-click restoration.
* **Dedicated Hardware Scanner (`DX2_Watch_Scanner.exe`) & Deep V4 Migration:** Detects connected `100VTECH` / DX2 removable drives, prevents accidental `C:\` deployment, and migrates existing `M0D V4\DATA` assets automatically.

---

## 📁 Folder Structure (`M0D V5`)

```text
M0D V5/
├── VTech MOD Station.exe          # Main M0D V5 (Eclipse) GUI application
├── DX2_Watch_Scanner.exe          # Standalone USB drive & DX2 signature scanner
├── Guide.txt                      # Quick-start user instructions
├── Backups/                       # Timestamped auto-snapshots & one-click restores
└── DATA/
    ├── App_Themes/                # Automatic date-based UI wallpapers (bg.jpg)
    │   ├── autumn/
    │   ├── christmas/
    │   ├── default/
    │   ├── halloween/
    │   ├── new_year/
    │   ├── spring/
    │   ├── summer/
    │   └── valentines/
    ├── Clock_Screen/              # Photo Clock Face files (PCF_0001.BIN)
    ├── Custom_Apps/               # Staging folder for Learning Lodge apps
    └── Logo/                      # Default 240x240 gallery logo (100_0001.jpg)
```

---

## 🚀 Quick Start

1. **Download or Build:**
   * Download the latest release (`Version 5 (Eclipse)`) from the [Releases](https://github.com/JustChill6/Project-DX2/releases/latest) page and extract it anywhere on your Windows PC (or run `M0D_V5_MAX.bat` to self-compile from source).
2. **Connect Your Watch:**
   * Slide the **Master Power Switch** on the back of your VTech KidiZoom DX2 to **ON**.
   * Connect the watch to your PC using a **Micro-USB data cable** (charge-only cables will not mount storage).
3. **Launch & Mod:**
   * Open **`VTech MOD Station.exe`** (or run **`DX2_Watch_Scanner.exe`** first to verify drive detection). The top status bar will show `Connected: <Drive> (100VTECH)`.
   * Run **Full Watch Backup** before making changes (automatic pre-deploy snapshots are also enabled by default).
   * When finished, use Windows **Safely Remove Hardware** before unplugging your watch.

---

## 📊 Hardware Compatibility Matrix

| Board / Revision | Region / Firmware ID | USB Mod Access (Tabs 1–3) | SP Flash / Preloader | Notes |
| :--- | :--- | :--- | :--- | :--- |
| **1938 / 1938A (v1.0)** | US / CA (`54-193800-000`) | **SUPPORTED** | **SUPPORTED** | Early PCB with unlocked MediaTek BootROM/Preloader COM port. |
| **1938B (Mid-Cycle)** | US / International | **SUPPORTED** | **LOCKED / PARTIAL** | Most units lock Preloader; full USB modding works normally. |
| **1938C (UK / EU)** | UK / EU (`54-193800-A03-000-S00`) | **SUPPORTED** | **BLOCKED** | Hardware-locked Preloader; full USB modding supported. |
| **1938 Late / DX3 / DX4** | Global Revisions | **SUPPORTED (Media)** | **BLOCKED** | Secure bootloader; `240×240` Baseline JPEGs & `.WAV` clips work. |

---

## ⚠️ Disclaimer

This project is an independent community modding tool and is not affiliated with, endorsed by, or associated with **VTech Holdings Limited**. Always back up your watch's `DCIM`, `VOICE`, and `VTE_DATA` folders before modifying files.
