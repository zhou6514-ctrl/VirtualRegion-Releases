# VirtualRegion Releases

## 中文

本仓仅用于发布 VirtualRegion 的安装包与更新元数据。

- 从 [Releases](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases/latest) 下载最新版 APK。
- `latest.json` 是管理器后台检查更新时读取的机器元数据。
- APK 只作为 GitHub Release 资产发布，不写入 Git 历史。
- 每次发布均记录 `versionCode`、`versionName`、下载地址和 APK 的 SHA-256。

下载后可使用 `latest.json` 中的 `sha256` 核对文件完整性。请仅从本仓 Releases 页面或应用内
系统下载入口获取安装包。

## English

This repository publishes VirtualRegion installation packages and update metadata only.

- Download the latest APK from [Releases](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases/latest).
- `latest.json` is the machine-readable manifest used by the manager's background update check.
- APKs are stored only as GitHub Release assets and are not committed to Git history.
- Each release records its `versionCode`, `versionName`, download URL, and APK SHA-256 digest.

After downloading, compare the file with the `sha256` value in `latest.json`. Obtain APKs only from
this repository's Releases page or through the manager's system-download action.
