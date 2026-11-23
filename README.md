<p align="center">
  <img src="./logobanner.png" alt="Project-DX2 Logo" />
</p>

# Project-DX2 — VTech MOD Station (M0D V4)

A lightweight, self-contained Windows desktop modding suite for the **VTech KidiZoom Smartwatch DX2** (`54-193800-A03-000-S00` and regional variants). Designed for safe USB Mass Storage modding—no risky firmware flashing required.

---

## ✨ What's New in M0D V4

* **Clean `DATA\` Folder Architecture:** All working directories (`Clock_Screen`, `Logo`, `Custom_Apps`, `App_Themes`, and `Backups`) live neatly inside a single `DATA\` subfolder, keeping the root folder clean and organized.
* **Automatic Seasonal UI Themes:** Reads your system date and time on launch and automatically applies custom seasonal backgrounds and accent colors (`Halloween`, `Christmas`, `New Year`, `Valentines`, `Spring`, `Summer`, `Autumn`, and `Default`) from `DATA\App_Themes\`.
* **5-Tab Top Navigation Layout:**
  1. **Watch Faces & Core:** Install custom `240×240` gallery logos (`100_0001.JPG`), inject/back up `PCF_0001.BIN` Photo Clock Faces, run full watch backups/restores, clean hidden macOS/Windows system junk (`._*`, `.DS_Store`, `Thumbs.db`), or reset to the stock clock face.
  2. **Apps, Games & Saves:** Inject Learning Lodge apps (`VTE_DATA\LL\APPS`), back up installed apps, export/import game & pedometer save data (`LL_SAVE`), and inspect watch storage capacity.
  3. **Audio & Media USB:** Single and batch `.WAV` sound/voice clip injection (`VOICE\100VTECH`), batch `240×240` strict Baseline JPEG conversion & import, automatic `DCIM` sequence renumbering, and full media export to PC.
  4. **DX2 Emulator:** Built-in `240×240` virtual DX2 screen simulator to preview live clock overlays, `PCF_0001.BIN` status, gallery slides, and custom images before ejecting your watch.
  5. **Availability:** Built-in hardware & COM port compatibility scanner that detects your connected DX2 board revision (`1938/1938A`, `1938B`, `1938C UK/EU`, or `DX3/DX4`) and highlights supported USB modding and Preloader access.
* **Zero-Dependency Self-Compiler:** Build `VTech MOD Station.exe` from scratch using `Build_M0D_V4.bat` via Windows' built-in .NET Framework 4.x compiler (`csc.exe`)—no Python or Visual Studio required.

---

## 📁 Folder Structure (`M0D V4`)

```text
M0D V4/
├── VTech MOD Station.exe          # Main M0D V4 GUI application
├── Guide.txt                      # Quick-start user instructions
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
    ├── Backups/                   # Auto-created watch, app, and LL_SAVE backups
    ├── Clock_Screen/              # Photo Clock Face files (PCF_0001.BIN)
    ├── Custom_Apps/               # Staging folder for Learning Lodge apps
    └── Logo/                      # Default 240x240 gallery logo (100_0001.jpg)
```

---

## 🚀 Quick Start

1. **Download or Build:**
   * Download the latest **`M0D V4.zip`** from the [Releases](../../releases) page and extract it anywhere on your Windows PC
2. **Connect Your Watch:**
   * Slide the **Master Power Switch** on the back of your VTech KidiZoom DX2 to **ON**.
   * Connect the watch to your PC using a **Micro-USB data cable** (charge-only cables will not mount storage).
3. **Launch & Mod:**
   * Open **`VTech MOD Station.exe`**. The top status bar will show `Connected: <Drive> (100VTECH)`.
   * Always run **Full Watch Backup** on Tab 1 before making changes.
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
