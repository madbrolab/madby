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

## 最新更新 0.3.19

- 片头按季复用，新集自动继承。没有季规则时最多抽查 3 集。至少 2 集有有效样本，且所有样本起止时间各相差不超过 2 秒，才取中间值用于整季。已有标记保留。
- 接入 TheIntroDB、SkipDB、AniSkip 和 IntroDB。外部数据默认关闭，与原生声纹、播放点击各有开关。外部优先，无可用季规则再用声纹，点击用于兜底和纠错。
- 媒体信息回退到原生探测后，失败一次就停止，并在待处理页显示原因。修复文件或挂载后可手动重试。
- 片头片尾识别可按名称多选媒体库。运行状态页支持分类、分页和查看单条失败详情。
- 修复删除外挂字幕后轨道仍然显示的问题。跳过视频探测时也会同步字幕轨道。

SHA-256

`584073e8f46c736fe5b8aaa2b7cf4f85582f6775405b13afef7f49a07e85d7ce`

## Install

1. Download `Madby.dll` from the latest release.
2. Copy `Madby.dll` into the Emby `plugins` directory.
3. Restart Emby.
4. Open the Madby plugin page in Emby and configure it.

## Note

This repository publishes only the project overview and release artifacts. Source code is not included.
