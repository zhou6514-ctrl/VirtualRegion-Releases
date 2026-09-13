# VirtualRegion

[中文](#中文) | [English](#english)

> [!WARNING]
> **使用地区限制 / Regional Usage Restriction**
>
> **中文：本模块不允许在中国使用，因此采用 Telegram 群组授权验证。**
>
> **English: This module is not permitted for use in China. Authorization is therefore verified through the Telegram group.**

## 中文

VirtualRegion 是一款面向 LSPosed 的手机环境虚拟化工具。它可以让不同应用看到各自独立的
位置、网络、手机卡、蓝牙、语言、时区和媒体内容，而不会把整台手机粗暴地改成同一套数据。

如果你经常做应用兼容测试、跨地区界面检查、路线演示或相机输入测试，VirtualRegion 能把原本
需要多台手机、反复改设置的工作，整理成一套可保存、可复用、可快速切换的配置。新手也不用面对
一堆难懂参数：先建环境，再选应用，最后点应用即可。

当前版本：[2.0.0](https://github.com/Xposed-Modules-Repo/io.github.zhou6514ctrl.virtualregion/releases/tag/200-2.0.0)

### 你可以用它做什么

#### 环境与地图

- 在地图上点选位置、搜索地点或直接输入坐标，也能一键回到真实位置。
- 保存多个环境，每个环境可以同时包含位置、Wi-Fi、基站和蓝牙信息。
- 从当前手机采集真实环境，减少手工填写；环境支持重命名、编辑、删除、导入和导出。
- 长按已保存环境即可快速应用；新增环境后也能直接选择要应用到哪些目标。
- 支持按应用生效，也支持全局环境模式。预览、保存和真正应用分开，不容易误操作。
- 环境广场支持浏览、搜索、分享和通过分享码导入环境，喜欢的配置可以先收藏到本地再决定是否使用。

#### 路线模拟

- 可通过地图绘制、路线规划或真实移动录制来创建路线。
- 路线支持预览、绑定、启动、暂停、继续、停止、调速和中断恢复。
- 播放路线时可同步位置、Wi-Fi、基站和卫星状态，让移动过程更连贯。
- 同一条路线可以分配给多个应用；“应用路线”和“应用并启动”分开，操作结果更可控。
- 提供路线控制悬浮窗，不必频繁切回管理器。

#### 按应用独立配置

- 每个应用都能单独选择环境或路线，并分别控制位置、Wi-Fi、基站、蓝牙等项目。
- 通过 UID、用户空间和包名区分主应用、双开应用与工作资料，不会只看名字混在一起。
- 支持应用搜索、系统应用筛选和全局模式；已启用项会优先显示。
- GPS 自然抖动可以模拟小范围的真实漂移，偏移距离可调，也能随时恢复默认值。

#### SIM、语言与时区

- 可设置应用看到的 SIM/eSIM、IMSI、ICCID、手机号、运营商、信号和基站信息。
- 没有实体 SIM 时也能创建独立的虚拟 SIM 配置。
- 语言和时区可以分别设置，也可一次设置两项或一键恢复跟随系统。
- 列表只显示已经加入 LSPosed 作用域的应用，支持搜索和显示系统应用，目标更容易找。
- 管理器界面语言与目标应用的虚拟语言完全独立，改其中一个不会连带修改另一个。

#### 虚拟媒体

- 支持 RTSP 与 RTMP 网络视频流，也支持手机里的本地视频和照片。
- 可分别替换应用的相机预览、录像画面、拍照结果和麦克风输入。
- 网络流首帧到达前显示加载画面，减少短暂露出真实相机画面的情况。
- 针对不同相机应用处理画面方向，改善前后摄像头切换、录制卡顿、声音杂音等体验。
- 照片输入模式保留真实麦克风；视频和网络流可使用媒体中的声音。
- 只展示已加入 LSPosed 作用域的目标应用，已启用应用排在前面。
- 媒体无法读取或解码失败时会回退真实相机和麦克风，避免拖垮目标应用。

#### 更顺手的管理器

- 全新侧滑导航，环境、路线、运行状态、应用、环境广场、作用域功能和设置都能直接进入。
- 支持浅色、深色和跟随系统主题，并处理状态栏、手势区域和横竖屏显示。
- 提供 18 种界面语言：简体中文、繁體中文、English、日本語、한국어、Русский、Español、
  Português（Brasil/Portugal）、Français、Deutsch、Italiano、Bahasa Indonesia、Tiếng Việt、ไทย、
  हिन्दी、العربية 和 Türkçe。
- 环境快捷切换、GPS 摇杆和路线控制三个悬浮窗可按需开启，最小化后不遮挡主要画面。
- 运行状态页集中显示服务状态、配置发送结果、日志和诊断，出现问题时更容易找到原因。
- 内置版本检查，有新版本时会展示更新内容并提供下载入口。

### 小白安装步骤

1. 从本页 Release 下载最新 APK 并安装。
2. 打开 LSPosed，在“模块”中启用 VirtualRegion。
3. 按模块提示勾选系统作用域；需要使用 SIM、语言/时区或虚拟媒体时，再勾选对应目标应用。
4. 重启手机，让系统服务加载新模块。
5. 打开 VirtualRegion，按提示完成授权。
6. 进入“环境与地图”创建环境，然后在应用管理或快捷应用面板选择目标应用。
7. 保存并应用后，彻底关闭再重新打开目标应用。

第一次使用建议先选一个不重要的测试应用。不同品牌、Android 版本和相机实现可能存在差异；
VirtualRegion 提供状态与诊断工具，但“已经保存”不一定等于目标应用进程已经重新读取配置，必要时
请重启目标应用或手机。

### 为什么值得试试

- **少折腾：** 常用环境、路线和媒体源保存一次即可反复使用。
- **更精细：** 不同应用可以看到不同配置，主应用、双开和工作资料也能分别处理。
- **看得懂：** 新界面把“保存了什么、应用给谁、是否已经发送”分开显示。
- **用途更完整：** 从固定位置、移动路线到相机与麦克风输入，一套工具覆盖更多测试场景。
- **失败可回退：** 配置缺失或媒体加载失败时优先保留真实系统行为，降低目标应用异常概率。

### 获取更新和帮助

Telegram：[https://t.me/VirtualRegion](https://t.me/VirtualRegion)

### 使用提醒

请只在自己拥有的设备，或已经得到设备与应用所有者明确许可的测试环境中使用。请勿用于欺骗、
身份冒用、规避访问控制、盗取信息、干扰他人或任何违法用途。

---

## English

VirtualRegion is an LSPosed environment virtualization tool. It lets different apps see their own
location, network, SIM, Bluetooth, language, time zone, and media inputs without forcing one global
set of values on the entire phone.

For compatibility testing, regional UI checks, route demonstrations, or camera-input testing,
VirtualRegion turns repeated device changes into reusable profiles. The workflow is simple: create
an environment, choose the apps, and apply it.

Current version: [2.0.0](https://github.com/Xposed-Modules-Repo/io.github.zhou6514ctrl.virtualregion/releases/tag/200-2.0.0)

### What you can do

#### Environments and maps

- Pick a place on the map, search for it, enter coordinates, or return to the real location.
- Save multiple environments containing location, Wi-Fi, cell, and Bluetooth data.
- Capture the current device environment and rename, edit, delete, import, or export profiles.
- Long-press a saved environment for quick apply, or choose targets immediately after creating one.
- Use per-app or global environment mode. Previewing, saving, and applying are kept separate.
- Browse, search, share, and import profiles from Environment Plaza before choosing whether to apply them.

#### Route simulation

- Create routes by drawing, route planning, or recording real movement.
- Preview, bind, start, pause, resume, stop, change speed, and recover interrupted recordings.
- Keep location, Wi-Fi, cell, and satellite status coordinated during playback.
- Assign one route to multiple apps, with separate “Apply” and “Apply and start” actions.
- Control active routes from an optional floating window.

#### Independent app profiles

- Give each app its own environment or route and enable location, Wi-Fi, cell, or Bluetooth separately.
- Distinguish main-user, cloned, and work-profile apps by UID, user, and package identity.
- Search apps, include system apps when needed, and use a dedicated global mode.
- Add adjustable natural GPS jitter for more realistic small position changes.

#### SIM, language, and time zone

- Configure the SIM/eSIM, IMSI, ICCID, phone number, carrier, signal, and cell data visible to apps.
- Create a virtual SIM profile even when no physical SIM is inserted.
- Set language and time zone separately, set both together, or restore system defaults in one tap.
- Search a list containing only apps already included in the LSPosed scope.
- Manager interface language is independent from the language virtualized for target apps.

#### Virtual Media

- Use RTSP or RTMP network streams, local videos, or local photos as media input.
- Replace camera preview, recorded video, captured photos, and microphone input independently.
- Show a loading frame before the first network frame to reduce brief real-camera exposure.
- Improve orientation across camera apps, front-camera switching, recording smoothness, and audio quality.
- Photo mode keeps the real microphone; video and network streams can use media audio.
- Show only LSPosed-scoped target apps, with enabled apps listed first.
- Fall back to the real camera and microphone if media loading or decoding fails.

#### A friendlier manager

- Open environments, routes, runtime status, apps, Environment Plaza, scoped features, and settings
  directly from the new drawer navigation.
- Choose light, dark, or system theme with system-bar and rotation support.
- Use 18 interface languages, including Simplified and Traditional Chinese, English, Japanese,
  Korean, Russian, Spanish, Brazilian and European Portuguese, French, German, Italian, Indonesian,
  Vietnamese, Thai, Hindi, Arabic, and Turkish.
- Enable optional environment switcher, GPS joystick, and route-control floating windows.
- Review service status, configuration delivery, logs, and diagnostics in one place.
- Receive a clear update prompt when a newer release is available.

### Beginner setup

1. Download and install the latest APK from Releases.
2. Open LSPosed and enable VirtualRegion under Modules.
3. Select the recommended system scope. Also select target apps that need SIM fallback,
   language/time-zone, or Virtual Media features.
4. Restart the phone so system services load the module.
5. Open VirtualRegion and complete authorization.
6. Create an environment, then choose targets in App Management or Quick Apply.
7. Save and apply, then fully close and reopen the target app.

Start with a non-critical test app. Behavior can vary by phone brand, Android release, and camera
implementation. A saved profile does not always mean an already-running target process has reloaded
it, so restart the target app or device when needed.

### Why try VirtualRegion

- **Less repetition:** save environments, routes, and media sources once and reuse them.
- **Fine-grained control:** configure different apps, clones, and work profiles independently.
- **Clear feedback:** distinguish what is saved, who it applies to, and whether it was delivered.
- **Broader workflows:** cover fixed locations, moving routes, camera content, and microphone input.
- **Safe fallback:** missing profiles or failed media loads prefer real system behavior to reduce app failures.

### Updates and help

Telegram: [https://t.me/VirtualRegion](https://t.me/VirtualRegion)

### Usage notice

Use VirtualRegion only on devices you own or in test environments where the device and app owners
have given clear permission. Do not use it for deception, impersonation, access-control bypass,
data theft, disruption, or any illegal activity.
