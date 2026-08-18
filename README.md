# VirtualRegion Releases

This is the dedicated binary release repository for
[VirtualRegion](https://github.com/zhou6514-ctrl/VirtualRegion).

- Download APKs from [GitHub Releases](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases/latest).
- `latest.json` is the machine-readable update manifest consumed by the manager app.
- Source code, build scripts, and issue tracking remain in the source repository.

APK files are intentionally stored as GitHub Release assets rather than committed into Git history.
Every published manifest includes `versionCode`, `versionName`, the APK URL, and its SHA-256 digest.

Use the publishing script in the source repository to update this repository. The Xposed module
listing repository is separate from both this binary repository and the source repository.
