# Kraken — P2P Download Manager & Torrent Engine

Kraken is a high-performance, ad-free BitTorrent client, media download manager, and self-hosted streaming server for Android. Built with Kotlin, Jetpack Compose, Material 3, and native C++ `libtorrent-rasterbar`, Kraken provides fast, battery-optimized torrent downloading, sequential video streaming, and media indexing without third-party ads or tracking.

---

## 🦑 Key Features & Subsystem Breakdown

### ⚡ BitTorrent Engine (`torrent-core`)
- **Current**: Native C++ `libtorrent-rasterbar` engine integration, Magnet link / `.torrent` file handling, DHT, PEX, LSD, NAT-PMP/UPnP port forwarding, and sequential download for instant playback.
- **Planned / Roadmap**: IP filtering / blocklist importer, protocol encryption enforce, and per-torrent bandwidth limits scheduler.

### 🎬 Sequential Streaming & Player (`stream`)
- **Current**: Play-while-downloading video stream server, Jetpack Media3 video playback, subtitle parsing (SRT/ASS), and Cast (Chromecast) support.
- **Planned / Roadmap**: On-the-fly video transcoding, audio track selection, and external player pass-through (VLC / MX Player).

### 📁 Download Manager & Storage (`storage`)
- **Current**: Background download service with battery & Wi-Fi-only guards, Storage Access Framework (SAF) SD card support, and category sorting.
- **Planned / Roadmap**: WebDAV / SMB network storage save targets, RSS feed auto-downloader, and automated torrent cleanup.

---

## 🏗️ Architecture & Technology Stack

- **Platform**: Android 13+ (minSdk 33, targetSdk 37).
- **UI & Controls**: Kotlin, Jetpack Compose, Material 3.
- **Torrent Engine**: Native C++ `libtorrent-rasterbar` (NDK JNI wrapper).
- **Media Stack**: Jetpack Media3, NanoHTTPd streaming server.
- **Licensing**: AGPL-3.0.

---

## 🛠️ Building & Running

```bash
./gradlew assembleDebug
./gradlew installDebug
```

---

## 📜 License

Kraken is released under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [`LICENSE`](LICENSE) for details.
