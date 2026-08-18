# VirtualRegion release repository contract

Read `.virtualregion-repository.json` first. This repository has role `release` and contains only
release documentation plus `latest.json`.

- Never add Android project code, signing keys, R8 mappings, or committed APK files here.
- Upload APK binaries as GitHub Release assets.
- Publish through the script declared by the matching machine contract so the release asset and
  `latest.json` remain consistent.
- Do not change an APK version on behalf of the user.
