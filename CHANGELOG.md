# Changelog

All notable changes to Hyde Music. Downloads are on the [Releases](https://github.com/Hyde-OpenSource/Hyde-Music-Andorid/releases) page.

## 6.2.0 — 2026-10-19

Highest-quality downloads, an updater that just works, and news from Hyde inside the app.

### New

- **Highest-quality downloads.** When you download a song, choose **Highest quality** (320 kbps, where available) or **Standard quality**. *Download all* picks the highest available for each song automatically.
- **Updates that just work.** A big update card appears on Home whenever an update is waiting. One tap downloads, installs and reopens Hyde. After your first in-app update, later updates install without Android's install screen (Android 12+).
- **News from Hyde.** Announcements and tips as a card, a Home banner, a notification or a “From Hyde” item in Settings — no app update needed.

### Fixed

- Background update downloads no longer stop partway through; they resume where they left off.
- Updates no longer always show Android's install screen.
- An update waiting for confirmation no longer sits on “Installing…” forever.

### Changed

- Update downloads are no longer Wi-Fi-only by default.
- New *Install automatically* switch in Settings › App › Software Update.

## 6.1.0 — 2026-10-19

More songs play, the Library is cleaner, there's a real shuffle button on the player, and you decide what's shared.

### New

- **A shuffle button on the player.** Right on the Now Playing screen, next to AI Shuffle.
- **Quick buttons on Library.** History, Stats and more are a tap away from the top of Library.
- **Clear privacy controls.** Anonymous analytics cover your device and app info only — never what you play or search — with a one-tap off switch in *Settings › App › Privacy*.

### Fixed

- **More songs just play.** Tracks blocked in your region — some remixes and acoustic versions like "Jhol Acoustic" — now find a playable source, and download too.
- **Maintenance screen button.** Its label was invisible; it now reads correctly, and remote changes apply without reopening the app.

### Changed

- **A cleaner Library.** Nearby Sync is gone, "Your Year" is tucked away until it's in season, and the list is shorter so your playlists stay in view.
- **Snappier pop and press animations** across the app.

## 6.0.2 — 2026-10-11

Playlists and imports work again, songs in long lists start sooner, and reloading is a pull.

### Fixed

- **Creating a playlist works.** New playlists were saved but never showed up in your library. They appear as soon as you create them, and "New Playlist…" in *Add to Playlist* works too.
- **Import from Spotify works.** Every link failed, because Spotify stopped accepting the anonymous access the app used. Hyde now reads the playlist's public page instead. Paste a public playlist link, tap *Fetch Playlist*, then *Save to Library*.
  - Spotify shares only the first 100 songs of a playlist this way. For a longer playlist, export it as a CSV file and use the CSV import below.
- **Import playlist from CSV works.** The songs in the file were never matched, so nothing was added. Hyde now reads the file, finds each song, and saves them as a new playlist named after the file. Supported: Exportify and TuneMyMusic exports, a plain `title,artist` list, M3U playlists, and text files with one `Title - Artist` per line.
- **Importing is faster.** Four songs are looked up at a time, and each match is no longer fetched twice.
- **Downloaded songs start sooner.** Tapping a song in a long list (Downloads, Liked Songs) made the app look up every song in the list one at a time before playing. It's now one lookup. A finished download also always plays straight from the download instead of asking for a stream first.
- **The refresh spinner is in the right place.** It showed inside the top bar and needed a very long pull. It now appears between the bar and the title after a normal pull.
- **Pull-to-refresh works on Library, Explore and History.** It never triggered there.

### Changed

- **Home's reload button is gone.** Pull down to reload.

### Install

- **Phone (arm64, almost every phone since 2017):** `HydeMusic-6.0.2-arm64-release.apk`
- **Any other device:** `HydeMusic-6.0.2-universal-release.apk`

Installs over 6.0.1 and earlier releases signed with the Hyde Open Source key, and keeps your library, playlists, downloads and settings. Or update from inside the app: *Settings › App › Software Update*.

## 6.0.1 — 2026-10-11

A quick update that makes lyrics feel right.

### Fixed

- **Lyrics change lines exactly on time.** Before, a line could switch up to a quarter of a second late because the app waited for the next position update. Each line change is now scheduled for the moment the line starts.
- **The interlude dots are smooth.** The three dots shown during instrumental breaks stuttered. They now move in step with your screen: they light up one by one, breathe gently, and shrink away just before the next line.
- **Word-by-word lyrics fill smoothly**, also in step with the screen. This applies to the karaoke sweep too.

### Even cooler

- **Only the line being sung animates.** The rest of the lyrics are redrawn only when the line changes. Nothing animates while music is paused or the lyrics are closed.
- **Fewer position updates.** The playback position now arrives four times a second only while the player, lyrics or ambient screen is open. Anywhere else it's once a second, since the mini player and lists don't show it. That cuts the work the app does in the background of every screen by about 75%.
- **Leaner image memory.** Covers are cached up to 64 MB / 300 images instead of 100 MB / 1000. Because 6.0 decodes covers at their display size, that still holds every cover on screen, with less memory churn while scrolling.

### Install

- **Phone (arm64, almost every phone since 2017):** `HydeMusic-6.0.1-arm64-release.apk`
- **Any other device:** `HydeMusic-6.0.1-universal-release.apk`

Installs over 6.0 and earlier releases signed with the Hyde Open Source key, and keeps your library, playlists, downloads and settings. Or update from inside the app: *Settings › App › Software Update*.

## 6.0 — 2026-10-10

The first full release of the new Hyde Music: a Liquid Glass interface on top of the proven Hyde playback engine.

### New

- **AI Shuffle.** A shuffle that flows: each next song is picked to follow the last one (shared artist, same album, similar length), never more than two in a row by the same artist, and a little randomness so no two shuffles match.
  - Player: the ✨ button under the volume slider turns AI Shuffle on or off for the current queue.
  - Playing Next: separate Shuffle and ✨ AI Shuffle toggles.
  - Playlists, albums and your library songs: a new **AI Shuffle** button next to Play and Shuffle, and in the long-press menu.
- **Suggested Songs under playlists.** Fresh YouTube Music picks based on what's in the playlist, skipping songs it already has. On your own playlists, tap **+** to add a song. You can also refresh the list, AI-shuffle the suggestions, or show more.
- **Reload Home.** A reload button in the Home header, and pull-to-refresh now works. Before this it never fired, and the engine sent back the old feed before the reload had started.
- **High refresh rate** switch (Settings › Appearance › Liquid Glass).

### Runs cooler

- **60 Hz by default.** The app used to run at the panel's full 120 Hz, so the GPU redrew the glass and backdrop shaders twice as often. Turn on *High refresh rate* if you want 90/120 Hz.
- **Lyrics** update about 30 times a second on a timer. Before, they redrew the whole player on every screen refresh (120 times a second).
- **Animated glow** background moves only while music is playing and the app is on screen, at about 12 frames a second. When paused or in the background it stops completely.
- **Artwork is decoded at the size it's shown.** Small list rows no longer decode full 544–1200 px covers, which means less CPU while scrolling and less memory. The blurred player background decodes a tiny 128 px copy.
- **SponsorBlock** checks the playback position only for songs that have segments. Before, it woke the CPU every second for every song.
- AI Shuffle itself scores a fixed sample of candidates per step, so even huge queues shuffle instantly on the main thread.

### Install

- **Phone (arm64, almost every phone since 2017):** `HydeMusic-6.0-arm64-release.apk`
- **Any other device:** `HydeMusic-6.0-universal-release.apk`

Signed with the Hyde Open Source release key. It updates any earlier Hyde Music release signed with the same key and keeps your library, playlists, downloads and settings.

## 5.5 — 2026-09-25

A support release for 5.0: a full audit of the codebase that fixed long-standing glitches, memory leaks and crashes, plus general optimisation.

## 5.0 — 2026-08-23 · "The New Look"

A brand-new interface with many UI changes across the app.

## Earlier

4.5, 4.1, 4.0 "The New Experience" and 3.5 "The Stability Release". See the [Releases](https://github.com/Hyde-OpenSource/Hyde-Music-Andorid/releases) page.
