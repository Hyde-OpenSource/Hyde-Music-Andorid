# 🎧 Hyde Music — By Tirth

A modern, fast and elegant music streaming app for Android, with a Liquid Glass interface, word-by-word lyrics and no ads.

**Latest: [Version 6.5.0](https://github.com/Hyde-OpenSource/Hyde-Music-Andorid/releases/latest)** · Also on [Windows & Linux](https://github.com/Hyde-OpenSource/Hyde-Music-Desktop) · [Website](https://www.hydeos.tech/music-docs.html) · [Changelog](CHANGELOG.md)

<p align="center">
  <img src="screenshots/lyrics.jpg" width="200" alt="Word-by-word lyrics">
  <img src="screenshots/now-playing.jpg" width="200" alt="Now Playing">
  <img src="screenshots/library.jpg" width="200" alt="Library">
  <img src="screenshots/search.jpg" width="200" alt="Search">
</p>

---

## ✨ What's new in 6.5.0

* Authentic original artwork, full-art inspection, and stable player cover sizing.
* Lighter Liquid Glass, stationary menus, and a welcome flow above all player chrome.
* Continue listening and up to six persistent Home shortcuts.
* AI Shuffle suggestions, density controls and Reshuffle.
* Optional audio-output EQ profiles and accessibility refinements.
* Listen Together timing, buffering, reconnect, participant-control and chat corrections.
* Cast playback controls now follow the receiver's real state and position.

Custom TV lyrics activation is deferred pending Google Cast registration.

Full notes: [CHANGELOG.md](CHANGELOG.md)

---

## 🎵 Features

* Stream unlimited music, ad-free
* Liquid Glass design, or a lighter *Performance* blur mode for older phones
* Word-by-word synced lyrics, translation and share cards
* Smart search with live suggestions
* Library: playlists, albums, artists, songs, downloads
* Offline downloads
* Sleep timer, playback speed and pitch, equalizer
* Cast / DLNA output, Listen Together
* In-app updates with checksum verification

<p align="center">
  <img src="screenshots/player-menu.jpg" width="200" alt="Player menu">
  <img src="screenshots/playlists.jpg" width="200" alt="Playlists">
  <img src="screenshots/settings.jpg" width="200" alt="Settings">
</p>

---

## 📦 Installation

1. Open the [latest release](https://github.com/Hyde-OpenSource/Hyde-Music-Andorid/releases/latest).
2. Download the APK for your phone:
   * `HydeMusic-<version>-arm64-release.apk` for almost every phone made since 2017 (smaller download)
   * `HydeMusic-<version>-0-universal-release.apk` if you're not sure, or the arm64 one won't install
3. Open the file and allow *Install unknown apps* for your browser or file manager if Android asks.

Already on Hyde Music? Install 6.5.0 over your current version to keep your library, playlists, downloads and settings. The release uses the same Hyde Open Source signing key as 6.2.1.

**Verify a download (optional):** compare `sha256sum <file>.apk` with `SHA256SUMS` in the release.

---

## 🔄 Updates

Hyde Music checks this repository for new releases. When one is out, you get a notification, and the update downloads, gets verified and installs from inside the app (*Settings › App › Software Update*).

---

## 🛠️ Tech Stack

* Flutter (Cupertino + Liquid Glass shaders, Impeller) for the interface
* Kotlin engine: Media3 / ExoPlayer playback, Room library, YouTube Music InnerTube client
* Riverpod state management

---

## ⚠️ Disclaimer

This application is intended for educational and personal use only.
All content is sourced from publicly available platforms.

---

## ❤️ Support

If you like this project, consider giving it a ⭐ on GitHub or [supporting development](https://www.hydeos.tech/donate.html).

~ Team Hyde · By Tirth and Hyde OpenSource
