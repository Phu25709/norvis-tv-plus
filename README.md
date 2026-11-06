# TV Nhà Plus

<p align="center">
  <img src="https://raw.githubusercontent.com/Phu25709/tv-nha-plus/main/tv_banner_art.jpg" alt="TV Nhà Plus banner" width="900" />
</p>

<p align="center"><strong>IPTV player cho Android TV, tối ưu remote và người dùng gia đình.</strong><br/>Android TV IPTV player designed for simple remote-first viewing.</p>
<table align="center">
  <tr>
    <td align="center"><strong>☕ Java</strong><br/><sub>Android app</sub></td>
    <td align="center"><strong>▦ XML</strong><br/><sub>Views & resources</sub></td>
    <td align="center"><strong>▶ Media3</strong><br/><sub>ExoPlayer IPTV</sub></td>
    <td align="center"><strong>⚙ Gradle</strong><br/><sub>APK build</sub></td>
  </tr>

<p align="center">
  <a href="https://github.com/Phu25709/tv-nha-plus/releases"><img src="https://img.shields.io/badge/Release-v0.2.27-7c3aed?style=flat-square&logo=github" alt="Release v0.2.27" /></a>
  <a href="https://developer.android.com/about/versions/oreo"><img src="https://img.shields.io/badge/Android-API%2026%2B-3ddc84?style=flat-square&logo=android&logoColor=white" alt="Android API 26+" /></a>
  <a href="https://www.java.com/"><img src="https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=openjdk&logoColor=white" alt="Java 17" /></a>
  <a href="https://developer.android.com/media/media3"><img src="https://img.shields.io/badge/Media3-ExoPlayer-4285f4?style=flat-square&logo=google" alt="Media3 ExoPlayer" /></a>
  <a href="https://github.com/Phu25709/tv-nha-plus"><img src="https://img.shields.io/badge/Project-Personal%20use-64748b?style=flat-square" alt="Personal use project" /></a>
</p>


<table align="center">
  <tr>
    <td align="center"><strong>🇻🇳 Tiếng Việt</strong><br/><sub>Hướng dẫn chính · Remote-first</sub></td>
    <td align="center"><strong>🇬🇧 English</strong><br/><sub>Quick start · Technical info</sub></td>
  </tr>
</table>\r\n## Tiếng Việt

### Tính năng

- Phát M3U/HLS và MPEG-TS trực tiếp trong app bằng Media3 ExoPlayer.
- Tự nhớ kênh đang xem, playlist và danh sách yêu thích.
- TV Guide có nhóm kênh, tìm kiếm, logo, EPG, audio track và phụ đề nhúng.
- OSD hiển thị độ phân giải, codec, FPS, bitrate và thông tin audio.
- Tự nhận diện luồng 50fps và yêu cầu Android TV đồng bộ tần số hiển thị khi thiết bị hỗ trợ.
- Tự làm mới playlist sau 30 phút mà không ngắt luồng nếu URL kênh không đổi.
- Shortcut Home cho VTV1, VTV3, VTV6, Live sự kiện và Giải Trí.
- Kiểm tra `update.json` ở chế độ nền; khi có bản mới app hiện thông báo cập nhật.

### Cách dùng

1. Cài APK lên Android TV/LEAP-S1.
2. Mở app, chọn **Thêm playlist M3U**.
3. Dán link M3U HTTP/HTTPS, rồi chọn **Tải danh sách**.
4. Khi đang xem: bấm **OK** để mở danh sách kênh; mũi tên lên/xuống để chuyển kênh; phím số để nhập số kênh.
5. Trong danh sách: giữ **OK** để thêm/bỏ yêu thích; bấm **Back** để quay lại kênh đang xem.

Link M3U mẫu được điền sẵn trong hộp thoại: `https://tinyurl.com/vmt47`.

### Điều khiển remote

| Nút | Tác vụ |
|---|---|
| OK khi đang xem | Mở TV Guide |
| OK trên kênh | Phát kênh |
| Giữ OK | Thêm/bỏ yêu thích |
| Lên/xuống | Chuyển kênh |
| Phím số | Dò theo số kênh |
| Trái/phải khi phát | Tua 10 giây nếu luồng có DVR |
| Back | Quay lại màn trước |

### Cập nhật ứng dụng

App đọc file `update.json` trên GitHub sau khi player mở. Nếu `versionCode` mới hơn bản đang cài, app hiển thị thông báo và mở link APK khi người dùng chọn **Cập nhật**. Lỗi mạng không làm gián đoạn việc xem TV.

## English

### Features

- Built-in M3U/HLS and MPEG-TS playback with Media3 ExoPlayer.
- Remembers the last channel, playlist and favourites.
- TV Guide with groups, search, logos, EPG, audio tracks and embedded subtitles.
- On-screen technical details: resolution, codec, FPS, bitrate and audio layout.
- Detects true 50 fps streams and requests a matching display refresh rate when Android TV supports it.
- Refreshes the playlist every 30 minutes without interrupting playback when the stream URL is unchanged.
- Home shortcuts for VTV1, VTV3, VTV6, Live Events and Entertainment.
- Background update check through `update.json` with an in-app update notification.

### Quick start

1. Install the APK on Android TV/LEAP-S1.
2. Open the app and choose **Thêm playlist M3U** (Add M3U playlist).
3. Paste an HTTP/HTTPS M3U URL and choose **Tải danh sách** (Load playlist).
4. While watching, press **OK** to open the channel list, use Up/Down to change channels, or enter a channel number.
5. In the guide, hold **OK** to toggle favourites and press **Back** to return to playback.

### Build

Requirements: Android SDK 34, JDK 17 and Gradle 8.9.

```powershell
gradle assembleDebug
gradle assembleRelease
```

- Application ID: `vn.hoanghoa.tvnhaplus`
- Current version: `0.2.27` (versionCode 29)
- APK: `TV-Nha-Plus-0.2.27.apk`
- Minimum Android version: Android 8 / API 26

## Công nghệ sử dụng / Technology stack

- **Java**: ngôn ngữ chính của ứng dụng Android.
- **Android Views + XML resources**: giao diện Android TV và tài nguyên hiển thị.
- **Media3 ExoPlayer 1.4.1**: phát HLS/M3U và MPEG-TS, đọc track video/audio/phụ đề.
- **Gradle Groovy**: cấu hình build và đóng gói APK.
- **JSON + HttpURLConnection**: manifest `update.json` và kiểm tra bản cập nhật nền.
## Ngôn ngữ giao diện / UI language

Bản hiện tại ưu tiên tiếng Việt để người lớn tuổi dùng dễ hơn. English documentation is included above. Full in-app Vietnamese/English switching is planned for the next localization pass so every Guide, settings and playback message is translated consistently.

## Compatibility and limitations

- Tested on Skyworth Formuler LEAP-S1, Android 14.
- Actual 4K, 50fps, Dolby Digital/5.1 playback depends on the stream, network, decoder, HDMI chain and TV/receiver.
- DRM, expiring links and streams requiring custom headers may not play.
- Playlist data stays in the app's private storage and is not embedded in the source repository.

## License

Personal research and home-use project. Check the rights and terms of each IPTV source before using or redistributing it.





