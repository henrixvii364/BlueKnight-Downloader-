<div align="center">

# ⚔️ Blue Knight Downloader

### Portable media downloader for Spotify, YouTube, TikTok, and Instagram

**One executable. No installation. No complicated setup.**

[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?logo=windows)](#system-requirements)
[![Platform](https://img.shields.io/badge/Platform-64--bit-blue)](#system-requirements)
[![Portable](https://img.shields.io/badge/Build-Portable-success)](#portable-usage)
[![Version](https://img.shields.io/badge/Version-1.0-purple)](#whats-new-in-v1.0)

</div>

---

## Overview

**Blue Knight Downloader** is a portable Windows application for downloading media from:

- 🎵 Spotify
- ▶️ YouTube
- 🎬 TikTok
- 📸 Instagram

It includes the required tools, supports local proxies, manages authentication inside the application, and keeps downloads organized by platform.

Python, `spotDL`, `yt-dlp`, and `FFmpeg` do not need to be installed separately.

---

## Features

### Multi-platform downloads

Download supported content from four major platforms:

| Platform | Supported content |
|---|---|
| Spotify | Tracks, albums, and playlists |
| YouTube | Videos, audio, playlists, and supported links |
| TikTok | Videos and supported posts |
| Instagram | Reels, posts, profiles, and supported media |

### Portable Windows application

- No installation required
- No separate Python installation
- Can be moved between folders or compatible Windows computers
- All required application files are included in the portable package

### Built-in authentication

Sign in directly inside the application when a platform requires authentication.

- No browser extension required
- No manual cookie-file export
- Authentication data is stored separately for each platform
- Sessions can be refreshed automatically when supported
- Credentials and sessions from different platforms are not mixed

### Improved YouTube compatibility

Blue Knight includes additional handling for YouTube restrictions such as:

```text
Sign in to confirm you're not a bot
```

The application can automatically switch between available request methods and authentication modes when necessary.

Some restricted, private, age-limited, or region-limited content may still require a valid account.

### Organized download folders

Downloads are stored inside:

```text
BlueKnightDownloader/
```

Each platform receives its own folder:

```text
BlueKnightDownloader/
├── Spotify/
├── YouTube/
├── TikTok/
└── Instagram/
```

This keeps downloaded audio, video, playlists, and related files separated and easy to find.

### Accurate download information

The interface displays real download information, including:

- Current progress
- Download speed
- Estimated remaining time
- Completed file count
- Failed file count
- Current file or item
- Final completion status

A download is only marked as completed after the expected output file has been created successfully.

### Dynamic interface

The interface includes:

- Light mode
- Dark mode
- Glass-style visual effects
- Platform-specific colors
- Dynamic backgrounds
- Separate workspaces for each supported service

Selecting a platform changes the appearance of the application to match that service.

### Bundled tools

The portable package includes:

- `yt-dlp`
- `spotDL`
- `FFmpeg`

Bundled tools are reused on every launch and are not downloaded again unnecessarily.

The application can also update or restore required tools automatically when supported.

### Fallback tool downloads

When a required tool is missing from a custom build, Blue Knight can cache it under:

```text
%LOCALAPPDATA%\BlueKnightDownloader
```

Independent fallback sources may be used:

| Tool | Fallback sources |
|---|---|
| spotDL | GitHub and SourceForge |
| yt-dlp | Official GitHub releases |
| FFmpeg | BtbN and gyan.dev |

Internet access is still required to resolve metadata and download online media.

### Proxy support

Blue Knight supports local HTTP and SOCKS5 proxies.

Compatible configurations include:

- v2rayN
- Clash
- Clash Verge
- Other HTTP proxy clients
- Other SOCKS5 proxy clients

The application includes:

- Proxy presets
- Manual proxy configuration
- HTTP proxy support
- SOCKS5 proxy support
- Built-in proxy testing
- Per-download proxy usage

Common v2rayN defaults:

```text
HTTP:   127.0.0.1:10809
SOCKS5: 127.0.0.1:10808
```

Your actual ports may differ depending on your proxy client configuration.

---

## What's New in v6.1

### Instagram support

Instagram now has a dedicated download workspace with support for:

- Reels
- Posts
- Profile links
- Supported media URLs
- Instagram-inspired interface colors

### Better YouTube restriction handling

The YouTube downloader can use alternative request configurations when YouTube displays bot-verification or sign-in restrictions.

### In-app sign-in

Users can authenticate directly inside Blue Knight without manually exporting browser cookies.

### Separate session storage

Each platform keeps its own authentication session and storage area.

### Improved file organization

Downloads from Spotify, YouTube, TikTok, and Instagram are automatically stored in separate folders.

### Improved progress reporting

Progress, file counts, speed, and estimated remaining time now reflect actual downloader activity more accurately.

### Updated interface

The application now includes redesigned platform pages, dynamic colors, light mode, dark mode, and improved visual feedback.

---

## Installation

Blue Knight Downloader does not require a traditional installation.

1. Download the latest ZIP package from the Releases page.
2. Extract the entire ZIP archive.
3. Keep all extracted files together.
4. Open:

```text
BlueKnightDownloader.exe
```

> [!IMPORTANT]
> Do not run the executable directly from inside the ZIP archive.

---

## Basic Usage

1. Open `BlueKnightDownloader.exe`.
2. Select Spotify, YouTube, TikTok, or Instagram.
3. Paste a supported URL.
4. Choose the preferred format or download options.
5. Configure a proxy when required.
6. Start the download.
7. Open the output folder when the download finishes.

---

## Spotify Usage

Paste a Spotify URL for a:

- Track
- Album
- Playlist

Spotify metadata is resolved through `spotDL`.

Depending on availability, audio may be matched using supported external audio providers.

---

## YouTube Usage

Paste a supported YouTube URL for a:

- Video
- Playlist
- Music video
- Audio download
- Supported channel or collection link

Available formats depend on the selected download mode and the media formats reported by YouTube.

---

## TikTok Usage

Paste a supported TikTok video or post URL.

Availability may depend on:

- Region
- Content visibility
- Login requirements
- TikTok platform changes

---

## Instagram Usage

Paste a supported Instagram URL for a:

- Reel
- Post
- Profile
- Supported media page

Private content requires an account that already has permission to view it.

---

## Signing In

When authentication is required:

1. Select the target platform.
2. Open the sign-in option inside the application.
3. Complete the sign-in process.
4. Close the authentication window when finished.
5. Retry the download.

Authentication data is stored separately for each service.

Do not share the application data folder if it contains an active login session.

---

## Proxy Configuration

To configure a proxy:

1. Open **Advanced Settings**.
2. Select **HTTP** or **SOCKS5**.
3. Enter the proxy host and port.
4. Select **Test Proxy**.
5. Start the download after a successful test.

Examples:

```text
HTTP://127.0.0.1:10809
SOCKS5://127.0.0.1:10808
```

Use the proxy address shown inside your proxy client.

---

## Portable Usage

Keep the executable and bundled application files in the same extracted folder.

You can move the complete folder to:

- Another directory
- Another disk
- A USB drive
- Another compatible Windows computer

Do not move only the executable unless the build is explicitly distributed as a single-file package.

---

## System Requirements

- Windows 10 or Windows 11
- 64-bit operating system
- Internet connection
- Sufficient free storage for downloaded media

Recommended:

- At least 4 GB of RAM
- Modern multi-core processor
- Stable internet connection
- Updated Microsoft Edge WebView2 Runtime for in-app authentication

---

## Package Structure

A typical release package may look like this:

```text
BlueKnightDownloader/
├── BlueKnightDownloader.exe
├── tools/
│   ├── ffmpeg/
│   ├── spotdl/
│   └── yt-dlp/
├── source/
├── downloads/
├── THIRD_PARTY_NOTICES.txt
├── LICENSE
└── README.md
```

The exact folder structure may vary between releases.

---

## Source Code

The original Python source code and proxy tests are included in:

```text
source/
```

Custom builds should preserve the required application assets and tool paths.

---

## Third-Party Components

Blue Knight Downloader uses third-party open-source tools, including:

- [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- [spotDL](https://github.com/spotDL/spotify-downloader)
- [FFmpeg](https://ffmpeg.org/)

Third-party licenses, notices, and source links are available in:

```text
THIRD_PARTY_NOTICES.txt
```

Blue Knight Downloader is not affiliated with Spotify, YouTube, Google, TikTok, ByteDance, Instagram, or Meta.

---

## Troubleshooting

### The application does not open

Confirm that:

- The ZIP archive was fully extracted
- The executable is not running from inside the ZIP
- All included files remain in the application folder
- Windows Defender or another antivirus did not remove a required file
- The application has permission to write to its folder

### A download fails immediately

Check that:

- The URL is valid
- The content is publicly accessible
- Your internet connection is working
- Your proxy configuration is correct
- The selected platform is available in your region
- The required authentication session is active

### YouTube requests account verification

Open the YouTube sign-in window inside Blue Knight and authenticate with an account that can access the requested content.

Some YouTube restrictions are controlled by YouTube and cannot always be bypassed without authentication.

### Instagram content cannot be downloaded

Confirm that:

- The link opens normally in a browser
- The post or profile is not private
- Your account has access to private content
- Your Instagram session has not expired

### Spotify metadata loads but audio fails

Spotify is used primarily for metadata resolution.

Audio matching and availability depend on the providers supported by `spotDL`, regional availability, and the accuracy of the track match.

### Proxy test fails

Confirm that:

- Your proxy client is running
- The selected proxy type is correct
- The host and port match the proxy client
- LAN or local connection access is enabled when required
- Another application is not blocking the local port

### A required tool is missing

Restart Blue Knight while connected to the internet.

The application will attempt to restore or cache the missing component using an available fallback source.

---

## Antivirus Notice

Portable applications that bundle download tools, Python components, network features, or process launchers may occasionally trigger false-positive antivirus detections.

Before running the application:

- Download it only from the official repository
- Verify the release checksum when provided
- Review the included source code
- Scan the release using your preferred security tools

Never disable antivirus protection permanently.

---

## Privacy

Blue Knight Downloader processes URLs and download operations locally whenever possible.

Authentication sessions may be stored locally so that users do not need to sign in repeatedly.

Users should:

- Protect their application data folder
- Avoid sharing active session files
- Sign out before giving the application folder to another person
- Remove cached sessions from shared computers

---

## Legal Notice

Blue Knight Downloader is intended for downloading content that you own, content that is publicly available, or content that you have permission to download.

Users are responsible for complying with:

- Copyright laws
- Platform terms of service
- Content licensing requirements
- Local regulations

The developers are not responsible for misuse of the application.

---

## Downloads

Download the latest release from the repository's **Releases** section:

```text
https://github.com/BlueKnightNet/BlueKnight-Downloader-/releases
```

Replace `USERNAME/REPOSITORY` with the correct GitHub repository path.

---

## Community

Telegram:

```text
@BlueKnight_Net
```

Use the repository Issues section to report:

- Bugs
- Failed downloads
- Interface problems
- Proxy issues
- Platform compatibility changes
- Feature requests

When reporting a problem, include the application version, platform, error message, and relevant log output.

---

<div align="center">

### ⚔️ The gates were locked. They are not locked anymore.

**Blue Knight Downloader v6.1**

</div>
