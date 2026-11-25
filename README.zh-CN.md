# 赤友NTFS助手（iBoysoft NTFS for Mac中文版）

[English](README.md) | **简体中文**

赤友NTFS助手是一款NTFS for Mac软件。macOS 默认可以读取 NTFS 硬盘，但不能直接写入。安装并按需挂载后，即可在原有 NTFS 格式上复制、编辑、删除和新建文件，无需先格式化，也适用于移动硬盘、U 盘以及 Boot Camp 分区。

[产品官网](https://aibotech.cn/ntfs-for-mac/) · [帮助文档](https://aibotech.cn/ntfs-for-mac/online-help.html)

[![Platform](https://img.shields.io/badge/platform-macOS-000000?logo=apple&logoColor=white)](https://aibotech.cn/ntfs-for-mac/)
[![macOS](https://img.shields.io/badge/macOS-27%20Golden%20Gate%20–%2010.13%20High%20Sierra-blue)](https://aibotech.cn/ntfs-for-mac/)

## 赤友NTFS助手能做什么？

- **直接读写 NTFS 硬盘。** 挂载后可在 NTFS 硬盘上新增、修改、删除和复制文件，无需先格式化。
- **支持自动挂载。** 扩展模式或高级模式完成首次授权后，后续连接硬盘可按该模式自动挂载。
- **三种挂载模式。** 可根据系统版本选择简单模式、扩展模式（FSKit，适用于 macOS 26 Tahoe及 macOS 27 Golden Gate）或高级模式（内核驱动）。
- **附带磁盘管理。** 可查看磁盘信息、挂载或推出磁盘、检查和修复磁盘，以及将硬盘格式化为 NTFS（格式化会删除全部数据，请先备份）。
- **支持 Boot Camp 分区。** 可读写双系统下的 Boot Camp NTFS 分区。
- **兼容范围较广。** 支持 Apple Silicon（包括已适配的 M1 至 M6 系列）和 Intel Mac，覆盖 macOS 10.13 High Sierra 至 macOS 27 Golden Gate，可用于常见的 NTFS 移动硬盘和 U 盘。

### 应该选择哪种挂载模式？

| 模式 | 技术路径 | 适用场景 | 说明 |
| --- | --- | --- | --- |
| 简单模式 | 基于 NFSv3 的用户态文件系统服务 | 偶尔使用、希望减少系统设置操作 | 每次连接硬盘后需在软件中手动挂载。 |
| 扩展模式（FSKit） | 通过苹果 FSKit 在用户空间运行文件系统扩展 | macOS 26 Tahoe 和 macOS 27 Golden Gate，希望减少传统内核驱动授权步骤 | 首次完成必要授权后，可按该模式自动挂载。 |
| 高级模式（内核驱动） | kext 类型的内核驱动 | 需要内核驱动、能接受较高授权门槛的工作流 | 需按系统提示允许系统扩展；Apple Silicon Mac 首次使用通常还可能需要进入恢复模式完成授权。完成后可自动挂载。 |

macOS 15 Sequoia 及更早版本不提供扩展模式，请根据软件提示选择简单模式或高级模式。完整的系统、芯片与模式关系见[兼容性说明](https://aibotech.cn/ntfs-for-mac/macos-compatibility.html)和[帮助文档](https://aibotech.cn/ntfs-for-mac/online-help.html)。

### 支持哪些平台和设备？

| 类别 | 支持范围 |
| --- | --- |
| 操作系统 | macOS 27 Golden Gate、26 Tahoe、15 Sequoia、14 Sonoma、13 Ventura、12 Monterey、11 Big Sur、10.15 Catalina、10.14 Mojave、10.13 High Sierra。macOS 10.8–10.12 需使用历史版本安装包 |
| Mac 机型 | Apple Silicon（包括已适配的 M1 至 M6 系列）和 Intel Mac；具体模式与授权要求可能因芯片而异 |
| 存储设备 | 通常可用于受支持的 NTFS 移动硬盘、U 盘及 Boot Camp 分区 |
| 文件系统类型 | 普通 NTFS；不能直接解锁或读写 BitLocker 加密盘 |

## 如何安装并开始使用？

1. 下载安装包（见下方下载说明）。
2. 打开 `.dmg` 并按向导完成安装。如果收到的是 `.zip`，请先双击解压出 `.dmg`。Mac App Store 版本会自动完成安装。
3. 启动软件并完成激活。官网版通常使用激活码：点击屏幕顶部菜单栏中的赤友 NTFS 助手图标，选择「激活软件」，粘贴注册码或激活码。官网版与 Mac App Store 版授权不互通，请使用对应渠道的软件版本。
4. 插入普通 NTFS 移动硬盘，在软件中选中该硬盘，点击「打开」，选择挂载模式，完成必要授权后点击「装载」。建议先用小文件测试读写。

启用 NTFS 读写不需要先格式化或擦除原有文件。

如果点击「打开」后没有出现模式选择窗口，请打开软件「设置」，取消勾选「不显示模式选择窗口，直接使用默认模式装载」。扩展模式或高级模式的额外授权步骤，请参阅[帮助文档](https://aibotech.cn/ntfs-for-mac/online-help.html)。

## 在哪里下载赤友NTFS助手？

当前官网介绍的版本为 **赤友NTFS助手 V9**（发布于 2026 年 9 月 10 日）。可从本仓库的最新 GitHub Release 下载 macOS 安装包（适用于 Apple Silicon 和 Intel）：

<https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/releases/latest/download/iBoysoft-NTFS-for-Mac.dmg>

备选官方下载：<https://aibotech.cn/download/downloadfile.php?p=ntfsformac&d=notrial_product_page&a=9997>

历史版本见 [Releases](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/releases) 页面。

## 版本历史是怎样的？

以下要点摘自官方[赤友NTFS助手版本发布历史与系统适配记录](https://aibotech.cn/ntfs-for-mac/release-history.html)。更早版本及完整说明请查看该页面。

### V9 — 2026年9月10日

- 采用苹果 FSKit 原生文件系统扩展框架，作为 macOS 26/27 的用户态方案。
- 支持 macOS 27 Golden Gate。

### V8 — 2025年7月30日

- 完成对 macOS 26 Tahoe 的适配，并在正式版发布前完成验证。
- 优化驱动架构，适配 macOS 26 Tahoe 的系统要求和安全策略。

### V7 — 2024年9月14日

- 以原生方式支持 macOS Sequoia 15，并在官方正式版发布前完成适配。
- 修复部分 UI 与权限引导逻辑，提升稳定性。

### V6 — 2023年9月25日

- 适配 macOS Sonoma 14。
- 新增繁体中文界面，并在 NTFS 磁盘右键菜单中集成快速操作。
- 支持 Mac M3 系列芯片；修复升级后注册状态异常等多项问题。

## 常见问题有哪些？

### Mac 能写入 NTFS 硬盘吗？

默认情况下不能。macOS 可以读取 NTFS 硬盘，但不能直接写入、修改或删除其中的文件。需要使用赤友NTFS助手这类 NTFS for Mac 工具，在硬盘能被识别的前提下完成挂载后，才能在原有格式上读写。

### 为什么我的移动硬盘在 Mac 上是只读的？

很可能是因为硬盘采用了 NTFS 格式，而 macOS 本身不能写入 NTFS。安装赤友NTFS助手，连接硬盘并选择一种读写模式挂载即可，不必先格式化。

### 要在 Mac 上使用 NTFS 硬盘，必须先格式化吗？

不必。赤友NTFS助手可以在保留现有文件的前提下读写 NTFS 硬盘，无需先转换成 APFS、HFS+、FAT 或 exFAT。

### 赤友NTFS助手可以安全使用吗？

在硬盘能够正常识别的前提下，它用于为普通 NTFS 硬盘启用读写，而不需要先格式化。它不能修复硬盘坏道、物理故障或分区损坏，也不能直接解锁 BitLocker 加密盘。请勿同时安装多款 NTFS 读写工具，以免驱动或挂载服务冲突。

### 支持 Apple Silicon Mac 和 Boot Camp 吗？

支持。官网帮助页写明可适配 Apple Silicon（包括已适配的 M1 至 M6 系列）和 Intel Mac，也可用于双系统下的 Boot Camp 分区。不同芯片和模式下的授权步骤可能不同，请以软件和系统提示为准。

### 能挂载 BitLocker 加密的 NTFS 硬盘吗？

不能。赤友NTFS助手及其他普通 NTFS for Mac 软件通常不能直接读写 BitLocker 加密的 NTFS 硬盘(在Mac上读写BitLocker加密盘，需使用另外的专门工具，比如iBoysoft BitLocker for Mac)。请不要按普通 NTFS 挂载流程处理这类磁盘，详见[帮助文档](https://aibotech.cn/ntfs-for-mac/online-help.html)。

### 如何卸载赤友NTFS助手？

请从软件菜单执行完整卸载，不要只把应用拖进废纸篓。卸载后，普通 NTFS 硬盘通常会恢复为 macOS 原生只读状态。完整步骤见[帮助文档](https://aibotech.cn/ntfs-for-mac/online-help.html)。

安装、激活、挂载模式、磁盘修复、格式化为 NTFS 及其他说明，请参阅[帮助文档](https://aibotech.cn/ntfs-for-mac/online-help.html)。

## 如何反馈问题或参与贡献？

如果使用中遇到问题，请先查阅[帮助文档](https://aibotech.cn/ntfs-for-mac/online-help.html)。也可发送邮件至 [support@aibotech.cn](mailto:support@aibotech.cn)，或通过微信公众号「赤友软件」联系客服。

- 报告缺陷请使用 GitHub 的 [Bug report](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/issues/new?template=bug_report.yml) 模板。
- 功能建议请使用 [Feature request](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/issues/new?template=feature_request.yml) 模板。
- 使用问题请到 [Discussions](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/discussions) 交流。
- 安全漏洞请按 [SECURITY.md](SECURITY.md) 进行私下报告，不要公开提交 Issue。

## 本项目使用什么许可证？

赤友NTFS助手是专有软件，适用[最终用户许可协议](https://aibotech.cn/software-license.html)。本仓库中的 [LICENSE](LICENSE) 为对应英文许可协议文本。这不是 MIT、GPL 等开源许可证。
