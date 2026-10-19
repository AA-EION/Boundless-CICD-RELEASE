# Boundless 1.0.0

Release pública 1.0.0 de **Boundless** — suite profesional de medición y análisis de audio para música, mastering, broadcast y cine de **EION STUDIOS**.

## Descargas

### macOS (Universal: Apple Silicon & Intel)

- **Instalador DMG**: `Boundless-1.0.0-macOS.dmg`
  - **SHA-256**: `<SHA256_MACOS_DMG>`
  - Compatible con macOS 26 (Tahoe) y posteriores.
  - Paquete Universal 2 nativo (`arm64` + `x86_64`).
  - Incluye `Install Boundless.pkg` y `Uninstall Boundless.command`.
  - Totalmente firmado con Apple Developer ID, notarizado y grapado (stapled) por Apple.

### Windows (x64)

- **Instalador Setup**: `Boundless-1.0.0-Windows-x64-Setup.exe`
  - **SHA-256**: `<SHA256_WINDOWS_EXE>`
  - Instalador para Windows 10/11 (`x64`).
  - Incluye plugins VST3, CLAP, AAX (PACE Eden wrapped y firmado) y aplicación Standalone.

---

## Formatos incluidos

Cada formato instala un único archivo contenedor que expone los **24 plugins de Boundless**:
- **VST3** (`Boundless.vst3`)
- **AU / Audio Unit (.component)** (`Boundless.component` — macOS)
- **CLAP** (`Boundless.clap`)
- **AAX** (`Boundless.aaxplugin` — Avid Pro Tools, firmado y wrapped con PACE Eden)
- **Aplicación Standalone** (`Boundless.app` / `Boundless.exe`)

---

## Firma y notarización

- **macOS**: Todos los binarios y el instalador cuentan con firma oficial **Apple Developer ID** (`Juan Gallego - D7V3TP96W4`), **Hardened Runtime** y están **completamente notarizados y grapados (stapled)** por Apple. El plugin AAX cuenta con la firma digital autorizada de **PACE Eden**. Instalación limpia y directa sin bloqueos de Gatekeeper.
- **Windows**: El bundle AAX lleva la firma digital de **PACE Eden** y carga en Pro Tools. El resto de binarios no llevan un certificado Authenticode de confianza pública: Windows SmartScreen mostrará un aviso de editor desconocido al ejecutar el instalador. Es esperado en esta versión. Para continuar: *"Más información" → "Ejecutar de todas formas"*.

---

## Changelog — 1.0.0 (Release inicial)

### 24 instrumentos en un único contenedor por formato
- **Boundless Suite**: Espacio de trabajo modular con paneles acoplables, divisores redimensionables, maximizado/pop-out por panel y 16 disposiciones de fábrica (incluyendo *Streaming Master*) además de gestión de layouts de usuario.
- **Variantes gráficas y numéricas independientes**: *Loudness* / *Loudness Numeric*, *Levels* / *Levels Numeric*, *Dynamics* / *Dynamics Numeric* y *Leq* / *Leq Numeric*.
- **Medidores especializados**: *History*, *Dynamics Timeline*, *Radar*, *Sound Field*, *Correlation*, *Spectrum*, *Spectrogram 2D*, *Spectrogram 3D* (superficie sombreada o cascada), *Pano Phase*, *Bit Monitor*, *Intelligibility*, *Peak Histogram*, *Monitor* y *Numbers*.
- **Relay entre pistas**: Envía audio de cualquier pista (downmix mono, L, R, C, Mid o Side) hacia el *Spectrogram* o *Intelligibility* de cualquier otra instancia de Boundless, reconectándose automáticamente por ID al reabrir la sesión.

### Estándares internacionales y multicanal hasta 9.1.6
- **Loudness**: ITU-R BS.1770-4, EBU R128 / Tech 3341 / 3342, ATSC A/85, ARIB TR-B32, OP-59 y objetivos de plataformas de streaming.
- **True Peak & Niveles**: Sobremuestreo 4× u 8×, PPM IEC 60268-10 (Tipo I y II, Nordic, BBC, EBU), VU IEC 60268-17 y escalas K-System (K-12, K-14, K-20).
- **Frecuencia, Leq e Inteligibilidad**: Ponderaciones Leq A, C, M y Z; bandas de octava IEC 61260; Speech Intelligibility Index (ANSI S3.5).
- **Formatos de canal**: Desde mono y estéreo hasta **9.1.6 Dolby Atmos**.

### Interfaz, rendimiento y licenciamiento
- **Motor DSP en doble precisión**: Hilo de audio 100% libre de bloqueos y asignaciones de memoria mediante triple buffer atómico; passthrough bit-exacto con 0 muestras de latencia.
- **Acabados de hardware**: Temas *Graphite* (oscuro) e *Ivory* (claro) y escalado de interfaz del 75% al 200%.
- **Protegido por Kuroko**: Prueba gratuita completa de 7 días en cada equipo, activación unificada para los 24 plugins y soporte de activación offline.
