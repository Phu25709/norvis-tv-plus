# Norvis TV Plus+

<p align="center">
  <img src="https://raw.githubusercontent.com/Phu25709/norvis-tv-plus/main/tv_banner_art.jpg" alt="Norvis TV Plus+ banner" width="900" />
</p>

<p align="center"><strong>An Android TV IPTV player designed for simple remote-first use.</strong></p>

<p align="center"><a href="README.md">🇻🇳 Tiếng Việt</a> · <a href="README.en.md">🇬🇧 English</a></p>

<p align="center">
  <a href="https://github.com/Phu25709/norvis-tv-plus/releases"><img src="https://img.shields.io/badge/Public%20release-v0.2.27-7c3aed?style=flat-square&logo=github" alt="Public release v0.2.27" /></a>
  <a href="https://developer.android.com/about/versions/oreo"><img src="https://img.shields.io/badge/Android-API%2026%2B-3ddc84?style=flat-square&logo=android&logoColor=white" alt="Android API 26+" /></a>
  <a href="https://www.java.com/"><img src="https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=openjdk&logoColor=white" alt="Java 17" /></a>
  <a href="https://developer.android.com/media/media3"><img src="https://img.shields.io/badge/Media3-ExoPlayer-4285f4?style=flat-square&logo=google" alt="Media3 ExoPlayer" /></a>
</p>

<table align="center">
  <tr>
    <td align="center"><strong>☕ Java</strong><br/><sub>Android application</sub></td>
    <td align="center"><strong>▦ XML</strong><br/><sub>Views and resources</sub></td>
    <td align="center"><strong>▶ Media3</strong><br/><sub>ExoPlayer IPTV</sub></td>
    <td align="center"><strong>⚙ Gradle</strong><br/><sub>APK packaging</sub></td>
  </tr>
</table>

## Features

- Built-in M3U/HLS and MPEG-TS playback with Media3 ExoPlayer.
- Remembers the last channel, playlist and favourites.
- TV Guide with channel groups, search, logos, EPG, audio selection and embedded subtitles.
- On-screen resolution, codec, FPS, bitrate and audio information.
- Detects 50 fps streams and requests a matching display refresh rate when Android TV supports it.
- Refreshes playlists every 30 minutes without interrupting playback when the stream URL is unchanged.
- Home shortcuts for VTV1, VTV3, VTV6, Live Events and Entertainment.
- Checks `update.json` in the background and notifies when a newer version is available.

## Quick install on Android TV / LEAP-S1

### With Downloader

Open Downloader on the TV and enter this code:

```text
2817291
```

This AFTVnews code downloads the APK through GitHub Releases CDN.

- Short URL: https://aftv.news/2817291
- APK: https://github.com/Phu25709/norvis-tv-plus/releases/download/v0.2.27/TV-Nha-Plus-0.2.29-qr-guide.apk

### Add a playlist

1. Open **Norvis TV Plus** and choose **Add M3U playlist**.
2. Paste an HTTP/HTTPS M3U URL and select **Load playlist**.
3. While watching, press **OK** to open the TV Guide; use Up/Down or channel number keys to switch channels.
4. In the Guide, hold **OK** on a channel to toggle favourites; press **Back** to return to playback.

The app pre-fills this sample link: `https://tinyurl.com/vmt47`.

### Remote controls

| Button | Action |
|---|---|
| OK while watching | Open the TV Guide |
| OK on a channel | Play the channel |
| Hold OK on a channel | Toggle favourite |
| Up/Down | Change channel |
| Number keys | Tune by channel number |
| Left/Right during playback | Seek 10 seconds when the stream provides DVR |
| Back | Return to the previous screen |

## Add a playlist from a phone over LAN

1. Connect the TV and phone to the same Wi-Fi/LAN.
2. On the TV Home screen, choose **Nhập từ điện thoại** (Import from phone) to show a QR code. In the TV Guide, **QR / Điện thoại** displays the pairing address.
3. Scan the QR code or enter the address shown on the TV in the phone browser.
4. Submit the playlist URL. The TV asks for confirmation before downloading and saving it.

The pairing page runs temporarily on the TV and receives data over the LAN. QuickChart generates the QR image, so the pairing URL (containing the TV's LAN address) is sent to that service to render the image; the playlist URL is sent directly from the phone to the TV. The importer currently supports M3U playlists; Xtream Codes credentials are not yet converted into a playlist.

## App updates

After the player opens, the app checks `update.json`. If its `versionCode` is higher than the installed version, the app notifies the user and opens the APK link when **Update** is selected. Network failures do not interrupt playback.

## Version and build

Latest local source/APK: **0.2.29**, versionCode **31**. Latest public GitHub release: **v0.2.27**.

Requirements: Android SDK 34, JDK 17 and Gradle 8.9.

```powershell
gradle assembleDebug
gradle assembleRelease
```

- Application ID: `vn.hoanghoa.tvnhaplus`
- Minimum Android version: API 26 (Android 8)
- Media3 ExoPlayer: 1.4.1

## Compatibility and limitations

- Checked on Skyworth Formuler LEAP-S1 running Android 14.
- 4K, 50 fps and Dolby Digital/5.1 playback depend on the source, network, decoder, HDMI chain and TV/receiver.
- DRM, expired links or sources requiring custom HTTP headers may not play.
- Playlists are stored in the app's private storage; personal playlist data is not included in the repository.

## License and IPTV sources

This project is for research and personal use. Check the rights and terms of each IPTV source before using or sharing it.
