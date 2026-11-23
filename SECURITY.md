# Security Policy

## Supported Versions

Only the latest release of **Project-DX2 (VTech MOD Station)** is actively maintained and supported with security and stability updates. Please ensure you are running the most recent version from the [Releases](../../releases) page before reporting an issue.

| Version | Supported |
| :--- | :--- |
| Latest Release | :white_check_mark: |
| Older Releases | :x: |

---

## Security & Hardware Safety Scope

**Project-DX2** is an open-source, offline Windows utility that interacts exclusively with local storage directories (`DCIM`, `VOICE`, and `VTE_DATA`) on connected VTech KidiZoom devices via standard USB Mass Storage.

* **No Network Activity:** The application makes zero external network connections, telemetry calls, or remote code downloads.
* **No Firmware Flashing:** Official releases do not bundle or execute low-level bootloader/Preloader flashing utilities.
* **Antivirus False Positives:** Because standalone `.exe` builds are compiled locally without a commercial code-signing certificate, Windows Defender or third-party antivirus tools may occasionally flag the binary heuristically. Users are encouraged to inspect the source code and compile the executable themselves using the included build script.

---

## Reporting a Vulnerability

If you discover a security vulnerability, data-corruption bug, or unintended file-handling behavior in this repository:

Contact The Email In The Description ASAP
