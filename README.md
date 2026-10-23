<div align="center">

# Boundless — Public Releases

**Reference-grade audio metering suite for music, mastering, broadcast, and cinema.**<br>
Every meter you need, unified in one plug-in file per format.

[![Latest Release](https://img.shields.io/github/v/release/AA-EION/Boundless-CICD-RELEASE?label=Latest%20Release&color=0f172a)](../../releases/latest)
[![Platforms](https://img.shields.io/badge/Platforms-Windows%2010%2F11%20%7C%20macOS%2026%2B-16a34a)](#deliverables)
[![Formats](https://img.shields.io/badge/Formats-VST3%20%7C%20AU%20%7C%20CLAP%20%7C%20AAX%20%7C%20Standalone-ea580c)](#supported-formats)
[![License](https://img.shields.io/badge/License-Proprietary-64748b)](https://eionstudios.com)

**A product of [EION STUDIOS](https://eionstudios.com) · Protected by [Kuroko](https://issen.kurokamicorp.com)**

</div>

---

## Overview

**Boundless** is a real-time, double-precision audio metering and analysis suite from **EION STUDIOS**, supporting channel layouts from mono through **9.1.6 immersive audio**. It passes audio through bit-identically with zero latency and zero coloration while providing 24 specialized instruments in a single shell per format:

- **Boundless Suite**: Modular, dockable workspace with 16 factory layouts (including *Streaming Master*) and custom user presets.
- **Loudness & Levels**: *Loudness* & *Loudness Numeric* (ITU-R BS.1770-4, EBU R128, ATSC A/85, ARIB, OP-59), *Levels* & *Levels Numeric* (True Peak 4×/8×, PPM Type I/II, BBC, EBU, VU, K-12/14/20), *Leq* & *Leq Numeric* (A, C, M, Z weightings), *History*, and *Peak Histogram*.
- **Dynamics**: *Dynamics*, *Dynamics Numeric*, *Dynamics Timeline*, and *Loudness Radar*.
- **Frequency & Intelligibility**: *Spectrum* (exact FFT & IEC 61260 octave bands), *Spectrogram 2D*, *Spectrogram 3D* (surface & waterfall), and *Speech Intelligibility Index* (ANSI S3.5).
- **Spatial & Diagnostic**: *Sound Field*, *Correlation*, *Pano Phase*, *Bit Monitor*, *Monitor*, *Numbers*, and inter-track **Relay**.

---

## Deliverables

👉 **[Download the latest release from GitHub Releases](../../releases/latest)**

| Platform | Architecture | Installer Package | Contents |
|---|---|---|---|
| **Windows 10 / 11** | `x64` (Intel / AMD) | `Boundless-<version>-Windows-x64-Setup.exe` | VST3, CLAP, AAX, Standalone |
| **macOS 26+** | Universal 2 (`arm64` + `x86_64`) | `Boundless-<version>-macOS.dmg` | `Install Boundless.pkg` (VST3, AU v2, CLAP, AAX, Standalone) & Uninstaller |

Each release includes SHA-256 checksums and platform signing details in the release notes.

Every release also carries `release-manifest.json`, which the EION Studios plug-in store and Launcher read to know which platforms the release offers and to verify each installer's SHA-256. A platform missing from it is shown as not available.

---

## Supported Formats

Boundless registers under the manufacturer **EION Studios** in your DAW plug-in browser. Every format is self-contained and statically linked.

| Format | Contents | Windows (`x64`) | macOS (`Universal 2`) |
|---|---|---|---|
| **VST3** | 24 plug-in classes | `C:\Program Files\Common Files\VST3\Boundless.vst3` | `/Library/Audio/Plug-Ins/VST3/Boundless.vst3` |
| **AU v2** | 24 Audio Unit components | — | `/Library/Audio/Plug-Ins/Components/Boundless.component` |
| **CLAP** | 24 native CLAP plug-ins | `C:\Program Files\Common Files\CLAP\Boundless.clap` | `/Library/Audio/Plug-Ins/CLAP/Boundless.clap` |
| **AAX** | 24 Pro Tools effects | `C:\Program Files\Common Files\Avid\Audio\Plug-Ins\Boundless.aaxplugin` | `/Library/Application Support/Avid/Audio/Plug-Ins/Boundless.aaxplugin` |
| **Standalone** | Full Boundless Suite | `C:\Program Files\EION Studios\Boundless\Boundless.exe` | `/Applications/Boundless.app` |

---

## Code Signing, Notarization & Integrity Verification

- **macOS**: Signed with an official **Apple Developer ID** certificate (Hardened Runtime), notarized by Apple, and stapled to both the installer `.pkg` and `.dmg`. AAX bundles are digitally wrapped and signed with **PACE Eden**. Installs cleanly without Gatekeeper warnings.
- **Windows**: AAX bundles are digitally wrapped and signed with **PACE Eden** for Avid Pro Tools. Verify all installer downloads against the SHA-256 hashes published in each release's notes:

```bash
# macOS
shasum -a 256 Boundless-*-macOS.dmg
```

```powershell
# Windows PowerShell
Get-FileHash -Algorithm SHA256 .\Boundless-*-Windows-x64-Setup.exe
```

---

## Licensing & Trial

- **7-Day Evaluation**: A full-featured 7-day trial begins automatically the first time Boundless runs on a machine (online or offline).
- **Single Activation**: Activating any single Boundless meter or the Standalone app unlocks all 24 plug-ins across all formats on that computer.
- **Offline Activation**: Studio computers without internet access can export an activation request directly from the plug-in's license window and import a signed `.kurokolic` file.

---

## Support

For product documentation, licensing inquiries, and technical support, visit **[eionstudios.com](https://eionstudios.com)**.

<div align="center">
<sub>Copyright © 2026 <b>EION STUDIOS</b> (永音). All rights reserved.</sub>
</div>
