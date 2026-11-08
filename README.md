# Norvis TV Plus+

<p align="center">
  <img src="https://raw.githubusercontent.com/Phu25709/tv-nha-plus/main/tv_banner_art.jpg" alt="Norvis TV Plus+ banner" width="900" />
</p>

<p align="center"><strong>Android TV IPTV player with a simple remote-first experience.</strong></p>

<p align="center">
  <a href="README.vi.md">🇻🇳 Tiếng Việt</a> · <a href="#english">🇬🇧 English</a>
</p>

## English

### Features

- Built-in M3U/HLS and MPEG-TS playback with Media3 ExoPlayer.
- Remembers the last channel, playlist and favourites.
- TV Guide with groups, search, logos, EPG, audio tracks and embedded subtitles.
- On-screen resolution, codec, FPS, bitrate and audio information.
- Detects true 50 fps streams and requests a matching display refresh rate when supported.
- Refreshes playlists every 30 minutes without interrupting playback when URLs are unchanged.
- Home shortcuts for VTV1, VTV3, VTV6, Live Events and Entertainment.
- Background update notification through `update.json`.

### Quick start

1. Install the APK on Android TV/LEAP-S1.
2. Open **Norvis TV Plus** and choose **Add M3U playlist**.
3. Paste an HTTP/HTTPS M3U URL and load it.
4. Press **OK** while watching to open the guide; use Up/Down or channel numbers to switch.

### Technology

- Java, Android Views/XML resources
- Media3 ExoPlayer 1.4.1
- Gradle Groovy
- Minimum Android API 26

### QR pairing research

The planned QR pairing flow will work on the same Wi-Fi/LAN: the TV shows a short-lived pairing QR, the phone opens a local setup page, and the M3U URL is sent directly to the TV for confirmation. Playlist URLs and tokens will not be sent to a public cloud service.

## Download

- [Latest APK release](https://github.com/Phu25709/tv-nha-plus/releases/latest)
- [Vietnamese README](README.vi.md)


## Cài nhanh trên Android TV / LEAP-S1

Dùng ứng dụng **Downloader** trên TV và nhập mã:

```text
2817291
```

Mã AFTVnews này tải APK Norvis TV Plus+ từ CDN GitHub Releases.

- Short URL: https://aftv.news/2817291
- APK CDN: https://github.com/Phu25709/norvis-tv-plus/releases/download/v0.2.27/TV-Nha-Plus-0.2.29-qr-guide.apk
