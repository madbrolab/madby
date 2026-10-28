# Madby

Madby is an Emby plugin release package. The current build is checked against official Emby 4.8.10.0, 4.9.5.0, 4.10.0.40 and 4.10.1.0 assemblies.

## Features

- dian115 FFP media-info injection with native Emby scan fallback.
- Media-info JSON snapshot persistence and restore.
- External subtitle scan and immediate registration after native Emby subtitle downloads.
- SubHD subtitle entry points.
- Movie multi-version merge.
- Missing primary image refresh for movies, series, seasons, episodes and videos.
- Chapter marker cleanup and media-library maintenance tasks.
- Memory cleanup and batch-task resource recovery.
- Optional hiding of media libraries with no indexed media items.
- Built-in auto update from GitHub Releases.

## Latest Build

Download:

- [Latest release](https://github.com/madbrolab/madby/releases/latest)

The release asset is a single plugin file: `Madby.dll`.

## 最新更新：0.3.16

- 修复通过 Emby“搜索字幕”下载 ASS 等字幕后只有文件、没有字幕轨道的问题；下载完成即登记，无需扫描媒体库。
- 支持字幕保存到媒体同目录或 Emby 内部元数据目录，自动失效对应目录缓存。
- 保留音视频轨道及索引，避免重复登记；关闭后台字幕扫描时，原生字幕下载仍正常登记。
- 统一原生探测回退、重试、超时与恢复状态处理。
- 深度删除会根据 STRM 内容删除 CD2 挂载目标及相关边车文件和空目录；删除整剧或整季时按 Emby 实际删除的每一集清理，删除单集时只清理该集，并严格限制在允许的根路径内。

验证范围：本地行为回归与官方程序集兼容性检查，不代表完整 Emby 服务实测。

SHA256:

`be7438cfda59613ca74e3143b759652ac515da29fcea4dc88222294c1f25e0e9`

Build size: `3522048 bytes`

## Install

1. Download `Madby.dll` from the latest release.
2. Copy `Madby.dll` into the Emby `plugins` directory.
3. Restart Emby.
4. Open the Madby plugin page in Emby and configure it.

## Note

This repository publishes only the project overview and release artifacts. Source code is not included.
