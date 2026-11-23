<p align="center">
  <img src="./logobanner.png" alt="Project-DX2 Logo" />
</p>

# Project-DX2 — VTech MOD Station (M0D V4)

A lightweight, self-contained Windows desktop modding suite for the **VTech KidiZoom Smartwatch DX2** (`54-193800-A03-000-S00` and regional variants). Designed for safe USB Mass Storage modding—no risky firmware flashing required.

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
   * Download the latest .zip from the [Releases](../../releases) page and extract it anywhere on your Windows PC
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
