# VirtualRegion release repository contract

Read `.virtualregion-repository.json` first. This repository has role `release` and contains only
release documentation plus `latest.json`.

- Never add Android project code, signing keys, R8 mappings, or committed APK files here.
- Upload APK binaries as GitHub Release assets.
- Publish through the script declared by the matching machine contract so the release asset and
  `latest.json` remain consistent.
- Do not change an APK version on behalf of the user.
- Accept only the final APK produced by the source repository's nmmp release script. Before any
  release, require valid APK signing, 16 KiB zip alignment, `libnmmp.so` and `libnmmvm.so` stored
  without compression for every packaged nmmp ABI, and build metadata proving at least the
  contract-required number of converted methods. Never publish the direct R8 intermediate APK.
- The APK uploaded here must be byte-identical to the APK uploaded to the configured LSPosed
  release repository. Update `latest.json` only after both uploads succeed.
- Release titles and notes are public, user-facing text. They may describe only behavior users can
  see. They must not mention nmmp, DEX/bytecode conversion, encryption, hardening, obfuscation,
  anti-tamper, anti-debugging, or equivalent implementation details.
