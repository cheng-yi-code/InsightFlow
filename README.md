InsightFlow
InsightFlow 是一个轻量级、无侵入式的 Android 性能监控 SDK。它通过 Hook 主线程消息调度，能够实时捕获 App 的卡顿现场，并提供堆栈信息记录与可视化查看功能，帮助开发者快速定位性能瓶颈。
核心功能
-无侵入初始化：利用 ContentProvider 实现 SDK 的自动初始化，业务方无需手动调用。
-实时卡顿监测：基于 Looper.setMessageLogging 监听主线程耗时，精准判定卡顿。
-故障堆栈抓取：卡顿时自动记录当前主线程堆栈信息，定位问题代码。
-数据可视化：内置简易报告页面，直接在 App 内查看历史卡顿记录。
技术亮点
-性能优先：采用单例内存缓冲区管理卡顿数据，减少 IO 开销。
-低耦合架构：监控核心逻辑与 UI 展示层分离，易于集成与扩展。
-深度排查：能够捕获并记录导致卡顿的具体函数调用路径。
使用方式
 1. 接入 SDK：将 InsightFlow 模块集成至 Android 项目中。
 2. 自动启动：SDK 会随 App 启动自动完成初始化，无需额外配置。
 3. 查看报告：在 App 中通过入口（例如菜单或悬浮球）跳转至 MonitorReportActivity，即可实时查看所有已捕获的卡顿记录及堆栈详情。

🚀 InsightFlow 性能监控 SDK


🔬 轻量级、无侵入的 Android 主线程卡顿监控工具

InsightFlow 能够帮助开发者轻松捕获 Android App 运行时的卡顿现场，提供毫秒级的卡顿耗时与完整的函数调用堆栈信息。


🌟 核心功能

🎯 零配置初始化: 利用 `ContentProvider` 实现 SDK 自动启动，业务方接入零代码。
⏰ 毫秒级监测: 监听主线程消息调度，精准捕捉耗时任务。
🔎 自动堆栈追踪: 卡顿发生时自动抓取主线程所有函数调用路径。
📊 内置可视化报告: 跨页面数据展示，支持直接在 App 查看历史卡顿记录。


📸 项目截图

1. App 内监控报告列表 
<img src="[https://img.imf.com/report_ui.png](https://github.com/user-attachments/assets/d3485d06-46eb-4273-800f-5adc2356c958)" width="300" /> 
2. 卡顿堆栈日志 (Logcat)
<img src="[https://img.imf.com/stacktrace_log.png](https://github.com/user-attachments/assets/9a154ad4-4593-4e98-99da-d0891da5e0ad)" width="300" /> 

🛠️ 技术原理

InsightFlow 深度挖掘 Android 框架特性：

初始化: 使用 `ContentProvider` 的生命周期特性。
监控核心: 挂钩 `Looper.setMessageLogging`，实时计算消息处理前后的系统时间差轴。
数据流: 使用 `MonitorDataStore`（单例 Object）作为内存中转站，实现监控逻辑与 UI 展示解耦。



📜 开源协议

This project is licensed under the MIT License - see the(cite: LICENSE) file for details.
