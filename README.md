# iBoysoft NTFS for Mac

**English** | [简体中文](README.zh-CN.md)

iBoysoft NTFS for Mac is a full-featured NTFS driver for macOS that enables full read and write access to Microsoft NTFS drives. macOS can only read NTFS by default; this tool lets you edit, copy, delete, and move files on NTFS disks in Finder without reformatting, including external drives and the Windows Boot Camp partition.

[Official Website](https://iboysoft.com/ntfs-for-mac/) · [Help Documentation](https://iboysoft.com/ntfs-for-mac/online-help.html)

[![Platform](https://img.shields.io/badge/platform-macOS-000000?logo=apple&logoColor=white)](https://iboysoft.com/ntfs-for-mac/)
[![macOS](https://img.shields.io/badge/macOS-27%20Golden%20Gate%20–%2010.13%20High%20Sierra-blue)](https://iboysoft.com/ntfs-for-mac/)

## What can iBoysoft NTFS for Mac do?

- **Full NTFS read and write.** Edit, delete, copy, and move files on NTFS drives, and use them in Finder like native Mac APFS or HFS+ disks.
- **Automatic writable mounting.** In Advanced mode, NTFS drives are mounted in read-write mode automatically when they are connected or at startup.
- **Flexible mounting modes.** Choose Simple mode, Extension mode (Apple's FSKit, macOS 26 and later, no kernel extension or restart), or Advanced mode (kernel-mode driver with automatic mounting).
- **Built-in disk management.** Open, eject, mount, unmount, repair, and format Windows drives; verify, open, and format non-NTFS volumes; and format drives to NTFS.
- **Boot Camp access.** Read and write the Windows BOOTCAMP NTFS partition directly, without reformatting.
- **Broad hardware and OS coverage.** Works on Apple Silicon (M5, M4, M3, M2, M1) and Intel Macs, from macOS 27 Golden Gate through macOS 10.13 High Sierra, with HDDs, SSDs, USB drives, SD cards, and all Microsoft NTFS versions from Windows NT 3.1 to Windows 10.

### Which mounting mode should I choose?

| Mode | How it works | When to use | Notes |
| --- | --- | --- | --- |
| Simple mode | Uses the NFS protocol and iBoysoft's own NTFS implementation | Quick read/write without extra setup | Remount the drive each time. The volume is not shown in the Finder sidebar and cannot be managed in Disk Utility. |
| Extension mode | Runs iBoysoft's NTFS file system in user space through Apple's FSKit | macOS 26 and later, when you want Finder access without a kernel extension or restart | Enable the `iboysoftntfs` extension once. After you replug the disk, open the app and click Mount again. |
| Advanced mode | Uses the iBoysoft NTFS driver in kernel mode for automatic mounting | Hands-off read/write whenever you connect a drive | On macOS 10.13 or later and on Apple Silicon Macs, enable the system extension. After that, you do not need to keep the app open. |

On macOS 15 Sequoia and earlier, only Simple mode and Advanced mode are available.

### Which platforms are supported?

| Category | Supported |
| --- | --- |
| Operating systems | macOS 27 Golden Gate, 26 Tahoe, 15 Sequoia, 14 Sonoma, 13 Ventura, 12 Monterey, 11 Big Sur, 10.15 Catalina, 10.14 Mojave, 10.13 High Sierra |
| Macs | Apple Silicon M5, M4, M3, M2, M1 (including Pro, Max, and Ultra variants listed on the product page) and Intel-based Macs |
| Storage | HDDs, SSDs, external hard drives, USB drives, SD cards, pen drives, flash drives, memory cards, CF cards, and other external drives |
| File systems | All Microsoft NTFS versions (Windows NT 3.1 through Windows 10) |

## How do I install and start using it?

1. Download the official `.dmg` installer (see the download section below).
2. Open the `.dmg` and follow the on-screen instructions. If you received a `.zip` file, double-click it first to reveal the `.dmg`.
3. On macOS 11 or later, allow the utility to access files in your Desktop folder when prompted the first time. After installation, the app opens automatically.
4. Click **Purchase & Activate** in the bottom-left corner of the main window, purchase a license if needed, then choose **Already Purchased?**, paste your license key, and click **Activate**. Keep an internet connection available during activation; temporarily pause a firewall or antivirus tool if it blocks registration.
5. Connect your NTFS drive, select it in the app, and click **Open** on the toolbar. Choose a mounting mode and click **Mount**. The drive then opens with read and write access.

You do not need to reformat the drive or erase data to write to NTFS on a Mac.

If the mode-selection dialog does not appear, open **iBoysoft NTFS for Mac** from the menu bar, go to **Settings > Advanced**, and uncheck **Mount directly without showing mode selection**. For the extra steps required by Extension mode or Advanced mode (enabling `iboysoftntfs` or the system extension), see the [Help Documentation](https://iboysoft.com/ntfs-for-mac/online-help.html).

## Where can I download iBoysoft NTFS for Mac?

The current official build advertised on the product page is **iBoysoft NTFS for Mac V9.0** (released September 8, 2026). Download the macOS installer (Apple Silicon and Intel) from this repository's latest GitHub Release:

<https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/releases/latest/download/iBoysoft-NTFS-for-Mac.dmg>

Alternative official download: <https://download.iboysoft.com/download/ntfsformac.dmg>

Previous versions are also available on the [Releases](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/releases) page.

## What is the version history?

Highlights below are taken from the official [Release History of iBoysoft NTFS for Mac](https://iboysoft.com/ntfs-for-mac/upgrade-history.html). For earlier releases, including V5.0 through V1.8, see that page.

### V9.0 — September 8, 2026

- Extension mode (macOS 26 and later) uses Apple's FSKit framework to run iBoysoft's NTFS file system in user space, with no kernel extensions required.
- Compatible with macOS 27 Golden Gate.
- Add iBoysoft Mac tool collection access.
- Improve performance and fix bugs.

### V8.0 — August 6, 2025

- Compatible with macOS 26 Tahoe and M5 Mac.
- Fix bugs.

### V7.0 — September 15, 2024

- Compatible with macOS 15 Sequoia.
- Fix bugs.

### V6.0 — September 25, 2023

- Compatible with macOS Sonoma.
- Fix bugs.

## What are the most common questions?

### Can Mac write to NTFS drives?

No. macOS can only read NTFS drives by default. Writing requires a third-party NTFS for Mac driver such as iBoysoft NTFS for Mac. This is not a macOS bug; NTFS is Microsoft's proprietary file system, and macOS disables write support for stability reasons.

### Why is my external hard drive read-only on Mac?

The drive is likely formatted as NTFS, which macOS cannot write to on its own. Install iBoysoft NTFS for Mac, connect the drive, and mount it in a read-write mode instead of reformatting.

### Do I need to reformat an NTFS drive to use it on a Mac?

No. With iBoysoft NTFS for Mac you can read and write the existing NTFS file system without erasing data or converting the drive to APFS, HFS+, FAT, or exFAT.

### Is iBoysoft NTFS for Mac safe to use?

Yes. Professional NTFS drivers such as this one are designed to allow safe read and write access without modifying the file system unsafely. You can write to NTFS drives without formatting them or running Terminal commands.

### Can I use it with Apple Silicon Macs and Boot Camp?

Yes. It supports Apple Silicon M5, M4, M3, M2, and M1 Macs as well as Intel Macs. It also provides direct read and write access to a Boot Camp NTFS partition. To start Windows from that partition, select it in the app and click **Startup** so Windows appears in Startup Disk.

### Can this tool mount BitLocker-encrypted NTFS drives?

No. iBoysoft NTFS for Mac does not mount BitLocker-encrypted drives. If the volume is encrypted with BitLocker, you need iBoysoft BitLocker for Mac to mount, read, and write it.

### How do I uninstall iBoysoft NTFS for Mac?

Open the app, click **iBoysoft NTFS for Mac** next to the Apple menu, and choose **Uninstall** to remove it completely. If you only deleted the app from the Applications folder, leftover driver components may remain; follow the complete-removal steps in the help documentation rather than deleting files by guesswork.

For installation, activation, mounting-mode setup, disk repair, erasing a disk to NTFS, and other how-to topics, see the [Help Documentation](https://iboysoft.com/ntfs-for-mac/online-help.html).

## How can I report a problem or contribute?

If something is not working, start with the [Help Documentation](https://iboysoft.com/ntfs-for-mac/online-help.html). You can also email [support@iboysoft.com](mailto:support@iboysoft.com) (Monday–Friday, 9:00–18:00, UTC+8).

- For bugs, open a GitHub issue with the [Bug report](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/issues/new?template=bug_report.yml) template.
- For feature ideas, use the [Feature request](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/issues/new?template=feature_request.yml) template.
- For usage questions, please use [Discussions](https://github.com/iBoysoft/iBoysoft-NTFS-for-Mac/discussions).
- For security vulnerabilities, follow the private reporting process in [SECURITY.md](SECURITY.md). Do not file a public issue.

## What license applies to this project?

iBoysoft NTFS for Mac is proprietary software licensed under the iBoysoft License Agreement (End User License Agreement). The full official text is in the [LICENSE](LICENSE) file in this repository and on the official [License Agreement](https://iboysoft.com/license-agreement.html) page. This is not an open-source license such as MIT or GPL.
