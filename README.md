# VirtualRegion

**用一台 Android 设备复现位置、网络和相机测试场景。**

**Reproduce location, wireless, and camera test scenarios on one Android device.**

[中文](#中文) · [English](#english) · [下载 / Download 2.1.6](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases/tag/v2.1.6)

> [!WARNING]
> **使用地区限制 / Regional Usage Restriction**
>
> **中文：本模块不允许在中国使用，因此采用 Telegram 群组授权验证。**
>
> **English: This module is not permitted for use in China. Authorization is therefore verified through the Telegram group.**

## 中文

VirtualRegion 是面向 LSPosed 的 Android 环境模拟工具。测试多语言界面、复现网络条件、演示移动路线，或给相机应用一段可重复的输入，都可以使用保存好的配置。选好场景、应用给目标，再用同一套条件复测。

[下载 VirtualRegion 2.1.6](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases/tag/v2.1.6) · [查看版本历史](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases) · [Telegram 社区](https://t.me/VirtualRegion)

### 构建场景，保存后随时复用

- **环境与地图**　用高德或 Google 地图搜索地点、点选位置、输入 WGS-84 坐标，也可以一键回到真实位置。地图定位超时时可回退到 Android 系统定位。采集设备附近的 Wi-Fi、基站、经典蓝牙和 BLE，或在地图选点生成 Wi-Fi 数据、查询附近基站。设置 GPS 抖动幅度，复现小范围的位置漂移。海拔优先使用实时结果，采用最近有效缓存时会标注来源。
- **管理与迁移**　位置和无线数据保存在同一份环境中，支持预览、编辑、重命名、导入、导出、快速应用和多选整理。可导入 Fake Location 的环境文件，或将系统保存的 SSID、加密类型等 Wi-Fi 数据加入环境。地图提供方及基站查询范围可在设置中调整。
- **环境广场**　按名称或地区搜索公开与私密环境，先在地图预览位置，再通过分享码或列表导入，也可分享自己的环境。常用场景留在本地，按需要应用。

### 让位置和连接一起变化

- **独立应用与全局模拟**　可为应用单独选择环境或路线，逐项控制 GPS、Wi-Fi、基站和蓝牙，按需启用严格隔离。主空间、双开和工作资料可以分别配置。支持应用搜索、筛选和快捷切换。全局模式适合多个应用共用同一场景，工作台总开关可保留配置并暂停或恢复环境模拟。
- **Wi-Fi、基站与蓝牙**　自定义 Wi-Fi 扫描列表、连接网络和信号，按信号自动选网，也可手动指定。为测试环境保存不同制式的基站记录，配置蓝牙设备、已绑定设备列表及 BLE 广播内容。需要复现扫描细节时，可编辑原始广播数据和扫描响应。
- **路线模拟**　在地图规划起终点，或录制真实路线，保存后可预览。录制可暂停、继续和恢复中断。为指定应用或全局范围选择路线并开始播放，随时暂停、继续、停止、调速、循环，或从当前位置重新规划终点。播放时可同步位置、Wi-Fi、基站和支持的卫星状态。GPS 摇杆可即时控制方向和速度。

### 把边界场景也纳入测试

- **SIM 与地区**　按订阅配置实体 SIM 或 eSIM 的测试数据，包括运营商、IMSI、ICCID、号码和信号。无实体 SIM 时可一键创建虚拟配置。语言和时区支持为应用分别设置、按地区模板应用及恢复系统值，可按国家、城市、语言代码或时区查找。
- **应用可见性**　按名称或包名搜索，并按 Android 用户空间设置隐藏应用列表，复现普通应用遇到依赖缺失的场景。页面可查看保存与生效状态，随时调整选择。
- **虚拟媒体**　把 RTSP、RTMP 网络流或本地视频和照片用作兼容应用的相机输入。可独立控制预览、拍照和麦克风替换，兼容录像链路支持媒体音轨及麦克风混音。支持前后摄像头切换时的画面方向适配，网络流加载时显示占位画面。照片模式保留真实麦克风，媒体不可用时回退到真实输入。

### 快捷操作和可见的运行状态

- **四个悬浮窗**　让测试应用保持前台，直接切换环境、操作 GPS 摇杆、控制路线或切换多段视频和图片。悬浮窗可随时收起，路线控制与管理器保持同步。
- **工作台与外观**　通过工作台、环境、应用、路线和更多入口定位常用功能，侧栏提供全部入口。配置编辑支持草稿恢复。支持浅色、深色及跟随系统，管理器可独立切换 18 种界面语言。
- **同步与诊断**　在状态页查看系统服务和配置同步进度，同步遇到问题时可重试。日志可筛选、复制和导出，崩溃报告可单独查看。管理器内置更新检查和下载入口。

### 2.1.6 新功能

- 环境列表输入即搜。单条或批量删除时，清理关联应用配置、解除路线关联并停止对应模拟。
- 在应用管理的全局配置中打开「系统应用生效范围」，勾选要使用全局环境的系统应用。模拟 Wi-Fi 可在手机未连接 Wi-Fi 时向目标应用呈现选定网络的已连接状态。
- 路线播放时可开启全局动作模拟，选择步行、跑步或驾车。加速度计、线性加速度和陀螺仪的波形频率随实时速度变化。播放停止后恢复原始动作数据。该功能适用于兼容设备上的普通传感器事件。
- 改善启动时的设置同步和 Xposed 兼容性。

### 快速上手

1. 在已 Root、支持 `arm64-v8a` 或 `armeabi-v7a` 的 Android 11 及以上设备上安装 APK，使用支持 Modern Xposed API 102 的框架启用模块。
2. 按模块推荐设置系统作用域。需要 SIM、语言与时区或虚拟媒体时，把相关目标应用加入 LSPosed 作用域。
3. 重启设备，打开 VirtualRegion 并按提示完成授权。
4. 保存一个环境或路线，选择目标，应用后在运行状态页确认配置已同步。对使用缓存的功能，重新打开目标应用以读取新配置。

具体支持范围取决于 Android 版本、厂商 ROM 及应用使用的接口。请在自有设备或明确授权的测试环境中使用。

---

## English

VirtualRegion is an Android environment simulation tool for LSPosed. Test localized interfaces, reproduce wireless conditions, demonstrate a route, or feed a repeatable clip to a camera app. Save the setup, apply it to your test targets, and reuse it on the next run.

[Download VirtualRegion 2.1.6](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases/tag/v2.1.6) · [Release history](https://github.com/zhou6514-ctrl/VirtualRegion-Releases/releases) · [Telegram community](https://t.me/VirtualRegion)

### Build a scenario once and reuse it

- **Environments and maps.** Search AMap or Google Maps, pick a location, enter WGS-84 coordinates, or return to the real location. Android location can provide a fallback on map location timeouts. Capture nearby Wi-Fi, cell, classic Bluetooth, and BLE data, or use a map selection to generate Wi-Fi entries and look up nearby cells. Adjust natural GPS drift. Altitude capture uses a live reading when available and labels a recent cached reading when used.
- **Manage and move profiles.** Keep location and wireless data in one saved environment. Preview, edit, rename, import, export, apply quickly, or select multiple environments for cleanup. Bring over Fake Location exports or add SSIDs and security types from saved system Wi-Fi networks. Choose the map provider and adjust the cell lookup radius in Settings.
- **Environment Plaza.** Search public and private environments by name or region, preview the location on a map, import from the list or with a share code, and share your own profiles. Keep useful profiles on the device until you need them.

### Move the location and wireless scene together

- **Per-app and global simulation.** Choose an environment or route for each app, control GPS, Wi-Fi, cell, and Bluetooth individually, and enable strict isolation as needed. Configure primary, cloned, and work-profile instances separately. Search and filter apps to change a setup quickly. Use global mode for a shared scenario. The home switch pauses or resumes environment simulation while keeping your settings.
- **Wi-Fi, cellular, and Bluetooth.** Set the Wi-Fi list, connection, and signal. Pick the connection by strength or choose it manually. Save cell records by radio technology, configure Bluetooth devices and bonded lists, and edit BLE advertisement and scan-response data.
- **Route playback.** Plan a route with map endpoints or record real movement and preview the saved route. Recordings support pause, resume, and recovery. Play a route for selected apps or globally. Pause, resume, stop, adjust the speed, loop, or plan a new destination from the current position. Playback can coordinate location, Wi-Fi, cells, and supported satellite status. Use the GPS joystick for quick direction and speed changes.

### Cover the edge cases of app testing

- **SIM and regions.** Configure test data for individual physical SIM or eSIM subscriptions, including carrier, IMSI, ICCID, number, and signal. Create a virtual profile on devices without a SIM. Set each app’s language and time zone independently, choose a region template, or restore system defaults. Search by country, city, language code, or zone.
- **App visibility.** Search by app or package name and manage hidden lists by Android user. Check how ordinary apps behave when a dependency appears unavailable. Review save and delivery status and adjust the selection when needed.
- **Virtual Media.** Use RTSP or RTMP streams, local videos, or photos as camera input. Control preview, photo capture, and microphone replacement separately. Compatible recording paths can use media audio or mix in the microphone. Orientation adapts on supported front and rear cameras, and a loading frame covers network startup. Photo mode keeps the real microphone, and unavailable media falls back to real input.

### Quick controls and clear feedback

- **Four floating tools.** Switch environments, steer the GPS joystick, control route playback, or switch between saved videos and photos while the test app stays in front. Minimize each tool when finished. Route controls stay in sync with the Manager.
- **Workspace and appearance.** Open the workspace, environments, apps, routes, and more from the main navigation, with the full feature list in the sidebar. Recover configuration drafts and choose light, dark, or system appearance. The Manager has 18 interface languages and its language can be set independently.
- **Synchronization and diagnostics.** Check system service and configuration delivery status, retry synchronization, filter, copy, or export logs, and review crash reports. Built-in update checks provide release notes and a download link.

### New in 2.1.6

- Filter saved environments as you type. Deleting one or multiple environments clears linked app settings, unlinks routes, and stops the affected simulation.
- Open **System app scope** in the global policy settings to include selected system apps in global mode. Simulated Wi-Fi presents the selected network as connected to target apps even when the phone is disconnected from Wi-Fi.
- Enable global motion simulation during route playback and choose walking, running, or driving. Accelerometer, linear acceleration, and gyroscope waveforms follow the live speed, with real readings restored after playback stops. This feature covers normal sensor event queues on compatible devices.
- Improved configuration synchronization at startup and Xposed compatibility.

### Quick setup

1. Install the APK on a rooted `arm64-v8a` or `armeabi-v7a` device with Android 11 or later. Enable the module in a framework that supports Modern Xposed API 102.
2. Select the recommended system scope. Include the target apps that need SIM, language and time zone, or Virtual Media features in the LSPosed scope.
3. Reboot, open VirtualRegion, and complete authorization.
4. Save an environment or route, choose the target, apply it, and check configuration delivery in runtime status. Reopen the target app when it caches settings.

Coverage depends on the Android version, ROM, and APIs used by the target app. Use VirtualRegion on your own devices or in an explicitly authorized test environment.
