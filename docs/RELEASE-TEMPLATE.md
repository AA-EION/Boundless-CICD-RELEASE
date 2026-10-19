# Plantilla de Release — Boundless (ES / EN)

Usa esta plantilla al publicar manualmente una nueva versión en **[GitHub Releases](../../releases/new)** o mediante `gh release create`.

---

## Opción A — Español (Formato oficial EION Studios)

````markdown
# Boundless <VERSION>

Release pública <VERSION> de **Boundless** — suite profesional de medición y análisis de audio de **EION STUDIOS**.

## Descargas

### macOS (Universal: Apple Silicon & Intel)

- **Instalador DMG**: `Boundless-<VERSION>-macOS.dmg`
  - **SHA-256**: `<SHA256_MACOS_DMG>`
  - Compatible con macOS 26 (Tahoe) y posteriores.
  - Binario Universal 2 nativo (`arm64` + `x86_64`).
  - Incluye `Install Boundless.pkg` y `Uninstall Boundless.command`.
  - Totalmente firmado con Apple Developer ID, notarizado y grapado (stapled) por Apple.

### Windows (x64)

- **Instalador Setup**: `Boundless-<VERSION>-Windows-x64-Setup.exe`
  - **SHA-256**: `<SHA256_WINDOWS_EXE>`
  - Compatible con Windows 10 y Windows 11 (`x64`).
  - Incluye selección personalizada de formatos: VST3, CLAP, AAX (PACE Eden wrapped y firmado) y aplicación Standalone.

---

## Formatos incluidos

Cada formato instala un único contenedor que expone los **24 medidores de Boundless** (Loudness, Levels, Dynamics, Leq, Spectrum, Spectrogram 2D/3D, Radar, Sound Field, Correlation, Pano Phase, Bit Monitor, Intelligibility, Peak Histogram, History, Dynamics Timeline, Monitor, Numbers y Relay):

- **VST3** (`Boundless.vst3`)
- **AU / Audio Unit v2** (`Boundless.component` — macOS)
- **CLAP** (`Boundless.clap`)
- **AAX** (`Boundless.aaxplugin` — Avid Pro Tools, firmado y wrapped con PACE Eden)
- **Aplicación Standalone** (`Boundless.app` / `Boundless.exe`)

---

## Firma y notarización

- **macOS**: Todos los binarios, el paquete instalador (`.pkg`) y la imagen de disco (`.dmg`) cuentan con firma oficial **Apple Developer ID** (`Juan Gallego - D7V3TP96W4`), **Hardened Runtime** y están **completamente notarizados y grapados (stapled)** por Apple. El bundle AAX cuenta con la firma digital autorizada de **PACE Eden**. Instalación limpia y directa sin avisos de Gatekeeper.
- **Windows**: El bundle AAX lleva la firma digital de **PACE Eden** y carga directamente en Pro Tools. El resto de binarios no llevan un certificado Authenticode de confianza pública: Windows SmartScreen mostrará un aviso de editor desconocido al ejecutar el instalador. Es esperado en esta versión. Para continuar: *"Más información" → "Ejecutar de todas formas"*.

Verifica la integridad de tus descargas comprobando el hash SHA-256 indicado arriba.

---

## Changelog

### Novedades y mejoras
- <Punto 1>
- <Punto 2>

### Correcciones
- <Corrección 1>
````

---

## Opción B — English

````markdown
# Boundless <VERSION>

Public release <VERSION> of **Boundless** — the professional audio metering and analysis suite by **EION STUDIOS**.

## Downloads

### macOS (Universal: Apple Silicon & Intel)

- **DMG Installer**: `Boundless-<VERSION>-macOS.dmg`
  - **SHA-256**: `<SHA256_MACOS_DMG>`
  - Supports macOS 26 (Tahoe) and later.
  - Native Universal 2 package (`arm64` + `x86_64`).
  - Contains `Install Boundless.pkg` and `Uninstall Boundless.command`.
  - Signed with Apple Developer ID, notarized, and stapled by Apple.

### Windows (x64)

- **Setup Installer**: `Boundless-<VERSION>-Windows-x64-Setup.exe`
  - **SHA-256**: `<SHA256_WINDOWS_EXE>`
  - Supports Windows 10 and Windows 11 (`x64`).
  - Includes VST3, CLAP, AAX (PACE Eden wrapped and signed), and the Standalone application.

---

## Included Formats

Each format installs a single shell binary exposing all **24 Boundless plug-ins** (Loudness, Levels, Dynamics, Leq, Spectrum, Spectrogram 2D/3D, Radar, Sound Field, Correlation, Pano Phase, Bit Monitor, Intelligibility, Peak Histogram, History, Dynamics Timeline, Monitor, Numbers, and Relay):

- **VST3** (`Boundless.vst3`)
- **AU / Audio Unit v2** (`Boundless.component` — macOS)
- **CLAP** (`Boundless.clap`)
- **AAX** (`Boundless.aaxplugin` — Avid Pro Tools, PACE Eden wrapped & signed)
- **Standalone Application** (`Boundless.app` / `Boundless.exe`)

---

## Code Signing & Notarization

- **macOS**: All bundles, the installer package (`.pkg`), and the disk image (`.dmg`) are signed with **Apple Developer ID** (`Juan Gallego - D7V3TP96W4`) with **Hardened Runtime**, and are **notarized and stapled** by Apple. The AAX bundle carries an authorized **PACE Eden** digital signature. Installs without Gatekeeper warnings.
- **Windows**: The AAX bundle is digitally wrapped and signed with **PACE Eden** and loads in Pro Tools. Other Windows binaries do not carry a public CA Authenticode certificate: Windows SmartScreen will display an unknown publisher prompt when launching the installer. Click *"More info" → "Run anyway"* to proceed.

Verify your downloads against the SHA-256 checksums listed above.

---

## Changelog

### Highlights
- <Highlight 1>
- <Highlight 2>

### Fixes
- <Fix 1>
````
