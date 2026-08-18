# VirtualRegion release repository contract

Read `.virtualregion-repository.json` first. This repository has role `release` and contains only
release documentation plus `latest.json`. Source changes belong in the configured source repository.

- Never add Android source code, signing keys, R8 mappings, or committed APK files here.
- Upload APK binaries as GitHub Release assets.
- Publish through `scripts/publish_apk_release.sh` in the source repository so the release asset and
  `latest.json` remain consistent.
- Do not change an APK version on behalf of the user. The source repository owns version values.
