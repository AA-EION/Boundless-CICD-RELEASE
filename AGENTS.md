# Notes for AI agents working in this repository

## Overview

Public release repository for **Boundless**. This repository hosts public documentation, release notes templates, payload guard scripts, and manually uploaded release installers. **It contains no application code, no packaging code, and no CI/CD workflows that call external repositories.**

## The layout rule

**Never add application or packaging code here.**

That includes `.cpp`, `.h`, `.mm`, `CMakeLists.txt`, `.cmake`, `.iss`, `.wxs`, project files, `src/`, `Source/`, `resources/`, `Resources/`, `packaging/`, `installer/`, `libs/`, and any certificate or key.

`scripts/guard_no_source.sh` enforces this rule. Run it before you commit:

```bash
./scripts/guard_no_source.sh
```

## Release model

All releases are built, signed, and verified locally on dedicated Windows and macOS machines and uploaded manually to GitHub Releases.

Before uploading a release directory, verify that only permitted installer files are present:

```bash
./scripts/verify_public_payload.sh <release-files-dir>
```

Use `docs/RELEASE-TEMPLATE.md` (or `docs/RELEASE-v1.0.0.md`) to compose the release notes.

## Testing a change

Changes can be checked locally:

```bash
./scripts/guard_no_source.sh
for f in scripts/*.sh; do bash -n "$f"; done
```
