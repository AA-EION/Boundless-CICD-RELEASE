<div align="center">

# Boundless — Public Releases

**Reference-grade audio metering suite for music, mastering, broadcast, and cinema.**<br>
Every meter you need, unified in one plug-in file per format.

[![Latest Release](https://img.shields.io/github/v/release/AA-EION/Boundless-CICD-RELEASE?label=Latest%20Release&color=0f172a)](../../releases/latest)
[![Platforms](https://img.shields.io/badge/Platforms-Windows%2010%2F11%20%7C%20macOS%2026%2B-16a34a)](#installers)
[![Formats](https://img.shields.io/badge/Formats-VST3%20%7C%20AU%20%7C%20CLAP%20%7C%20AAX%20%7C%20Standalone-ea580c)](#supported-formats)
[![License](https://img.shields.io/badge/License-Proprietary-64748b)](https://eionstudios.com)

**A product of [EION STUDIOS](https://eionstudios.com) · Protected by [Kuroko](https://issen.kurokamicorp.com)**

</div>

---

## Download

👉 **[Download Boundless at plugins.eionstudios.com](https://plugins.eionstudios.com)**

That page always has the current version for your system. The same installers are also attached to this repository's **[GitHub Releases](../../releases/latest)**.

---

## Overview

**Boundless** is a real-time, double-precision audio metering and analysis suite from **EION STUDIOS**, supporting channel layouts from mono through **9.1.6 immersive audio**. It passes audio through bit-identically with zero latency and zero coloration while providing 24 specialized instruments in a single shell per format:

- **Boundless Suite**: Modular, dockable workspace with 16 factory layouts (including *Streaming Master*) and custom user presets.
- **Loudness & Levels**: *Loudness* & *Loudness Numeric* (ITU-R BS.1770-4, EBU R128, ATSC A/85, ARIB, OP-59), *Levels* & *Levels Numeric* (True Peak 4×/8×, PPM Type I/II, BBC, EBU, VU, K-12/14/20), *Leq* & *Leq Numeric* (A, C, M, Z weightings), *History*, and *Peak Histogram*.
- **Dynamics**: *Dynamics*, *Dynamics Numeric*, *Dynamics Timeline*, and *Loudness Radar*.
- **Frequency & Intelligibility**: *Spectrum* (exact FFT & IEC 61260 octave bands), *Spectrogram 2D*, *Spectrogram 3D* (surface & waterfall), and *Speech Intelligibility Index* (ANSI S3.5).
- **Spatial & Diagnostic**: *Sound Field*, *Correlation*, *Pano Phase*, *Bit Monitor*, *Monitor*, *Numbers*, and inter-track **Relay**.

---

## Installers

| Platform | Architecture | Installer | Contents |
|---|---|---|---|
| **Windows 10 / 11** | Universal (`x64` + `ARM64`) | `Boundless-<version>-Windows-Universal-Installer.exe` | VST3, CLAP, AAX, Standalone |
| **macOS 26+** | Universal 2 (`arm64` + `x86_64`) | `Boundless-<version>-macOS-Universal.dmg` | `Install Boundless.pkg` (VST3, AU v2, CLAP, AAX, Standalone) and `Uninstall Boundless.command` |

AAX is x64 only and is hidden automatically on Windows ARM64.

Every release also carries `release-manifest.json`, which lists each installer with its size and SHA-256. The plug-ins' update check, the EION Studios plug-in store and the Launcher read only that file.

---

## Supported Formats

Boundless registers under the manufacturer **EION Studios** in your DAW plug-in browser.

| Format | Windows | macOS |
|---|---|---|
| **VST3** | `C:\Program Files\Common Files\VST3\Boundless.vst3` | `/Library/Audio/Plug-Ins/VST3/Boundless.vst3` |
| **AU v2** | — | `/Library/Audio/Plug-Ins/Components/Boundless.component` |
| **CLAP** | `C:\Program Files\Common Files\CLAP\Boundless.clap` | `/Library/Audio/Plug-Ins/CLAP/Boundless.clap` |
| **AAX** | `C:\Program Files\Common Files\Avid\Audio\Plug-Ins\Boundless.aaxplugin` | `/Library/Application Support/Avid/Audio/Plug-Ins/Boundless.aaxplugin` |
| **Standalone** | `C:\Program Files\EION Studios\Boundless\Boundless.exe` | `/Applications/Boundless.app` |

---

## Updates

When a new version is published here, Boundless tells you inside the plug-in and opens **[plugins.eionstudios.com](https://plugins.eionstudios.com)**, where you download and run the new installer. It installs over the previous version and keeps your license, settings and presets.

---

## Code Signing, Notarization & Integrity

- **macOS**: signed with an **Apple Developer ID** certificate (Hardened Runtime), notarized by Apple and stapled to both the `.pkg` and the `.dmg`. AAX bundles are wrapped and signed with **PACE Eden**. Installs without Gatekeeper warnings.
- **Windows**: AAX bundles are wrapped and signed with **PACE Eden** for Avid Pro Tools. The other binaries carry no public Authenticode certificate, so Windows SmartScreen shows an unknown-publisher prompt: choose *More info → Run anyway*.

Check a download against the SHA-256 in the release notes:

```bash
# macOS
shasum -a 256 Boundless-*-macOS-Universal.dmg
```

```powershell
# Windows PowerShell
Get-FileHash -Algorithm SHA256 .\Boundless-*-Windows-Universal-Installer.exe
```

---

## Licensing & Trial

- **30-day evaluation**: a full-featured 30-day trial starts automatically the first time Boundless runs on a computer, online or offline (Boundless 1.1.0 and earlier: 7 days).
- **Single activation**: activating any Boundless meter or the Standalone app unlocks all 24 plug-ins in every format on that computer.
- **Offline activation**: studio computers without internet can export an activation request from the plug-in's license window and import a signed `.kurokolic` file.

---

## Support

For documentation, licensing and technical support, visit **[eionstudios.com](https://eionstudios.com)**.

<div align="center">
<sub>Copyright © 2026 <b>EION STUDIOS</b> (永音). All rights reserved.</sub>
</div>
