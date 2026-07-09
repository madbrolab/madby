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
- Built-in auto update from GitHub Releases.

## Latest Build

Download:

- [Latest release](https://github.com/madbrolab/madby/releases/latest)

The release asset is a single plugin file: `Madby.dll`.

## Latest Update

- Deep delete now removes the CD2-mounted target file referenced by the deleted STRM, plus related sidecar files and empty folders, while staying inside the configured allowed roots.
- The deep-delete root picker can use the CD2 mount prefix resolved from dian115 through the configured OpenAPI key.
- The log page has been reorganized into compact status sections and includes a full history cleanup action.
- The default ffprobe wait time for FFP is now 10 seconds.
- Plugin tabs are localized in Chinese again.

SHA256:

`F625B1D6B79051FA88B5E941FC75E3CB8466BAD22BCDF1609570230F30B6B8D0`

## Install

1. Download `Madby.dll` from the latest release.
2. Copy `Madby.dll` into the Emby `plugins` directory.
3. Restart Emby.
4. Open the Madby plugin page in Emby and configure it.

## Note

This repository publishes only the project overview and release artifacts. Source code is not included.
