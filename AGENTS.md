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

Use `docs/RELEASE-TEMPLATE.md` to compose the release notes.

## Every release carries `release-manifest.json` (required)

The plug-in store and the EION Studios Launcher read **only**
`release-manifest.json`, attached to each release, to learn the release's
version, which platforms it has and each installer's size and SHA-256. A
platform the manifest does not list is shown as **not available**; a release
without the file, or with one that does not match its installers, is rejected
by the store.

1. **Every release has `release-manifest.json` next to the installers.**
2. **It is generated in the private product repository** with
   `tools/make_release_manifest.py --dist <folder>` from the folder holding
   exactly the files to upload. Never write or edit it by hand.
3. **Verify the folder before uploading**; this also checks the manifest
   against every installer in it:

   ```bash
   ./scripts/verify_public_payload.sh <release-files-dir>
   ```

4. **Whenever the installers of a published release change** (a platform
   added later, an installer replaced or removed), regenerate the manifest in
   the product repository (`--merge` with the attached copy keeps the other
   platforms) and upload it together with the installer, replacing the old
   one:

   ```bash
   ./scripts/verify_public_payload.sh <folder-with-new-installer-and-manifest> --adding
   gh release upload <tag> <new installer> <folder>/release-manifest.json --clobber
   python3 scripts/verify_release_manifest.py --github <tag> --repo <owner>/<this-repository> --product boundless
   ```

5. The tag is the version (`1.2.3` or `v1.2.3`) and must equal the manifest's
   `version`.

`.github/workflows/release-manifest.yml` re-checks every release when it is
published or edited and fails when the manifest is missing or out of date.
The contract is `shared/schema/release-manifest.schema.json` in
`AA-EION/EION-STUDIOS-PLUGIN-LAUNCHER`.

## Testing a change

Changes can be checked locally:

```bash
./scripts/guard_no_source.sh
python3 -m py_compile scripts/*.py
for f in scripts/*.sh; do bash -n "$f"; done
```
