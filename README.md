# Madby

Madby is an Emby plugin release package for Emby 4.9.x environments.

## Features

- dian115 FFP media-info injection with native Emby scan fallback.
- Media-info JSON snapshot persistence and restore.
- External subtitle scan and registration.
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

## 最新更新

- 新增“隐藏无媒体的媒体库”开关，只处理真正的 `CollectionFolder`。
- 使用 Emby 数据库递归查询判断是否存在非文件夹媒体，不扫描文件系统目录树，也不删除任何媒体库或文件。
- 按当前用户的可见权限判断；合集、播放列表、Live TV、频道等特殊视图不会被误隐藏。
- 查询异常时保留原始媒体库列表，并使用短时缓存和媒体变更失效机制，避免影响 Emby 正常运行。
- 深度删除会根据 STRM 内容删除 CD2 挂载目标及相关边车文件和空目录，并严格限制在允许的根路径内。
- 默认 ffprobe 等待时间为 10 秒，插件页面 TAB 已恢复中文显示。

SHA256:

`AC07DB8E16FA6DCACD6A1C08F2112E1E8C5AC0CFDFB8F8916834DB1753EC7176`

Build size: `3312640 bytes`

## Install

1. Download `Madby.dll` from the latest release.
2. Copy `Madby.dll` into the Emby `plugins` directory.
3. Restart Emby.
4. Open the Madby plugin page in Emby and configure it.

## Note

This repository publishes only the project overview and release artifacts. Source code is not included.
