# Norvis TV Plus+

<p align="center">
  <img src="https://raw.githubusercontent.com/Phu25709/norvis-tv-plus/main/tv_banner_art.jpg" alt="Norvis TV Plus+ banner" width="900" />
</p>

<p align="center"><strong>Trình phát IPTV cho Android TV, tối ưu thao tác remote.</strong></p>

<p align="center"><a href="README.md">🇻🇳 Tiếng Việt</a> · <a href="README.en.md">🇬🇧 English</a></p>

<p align="center">
  <a href="https://github.com/Phu25709/norvis-tv-plus/releases"><img src="https://img.shields.io/badge/Public%20release-v0.2.27-7c3aed?style=flat-square&logo=github" alt="Public release v0.2.27" /></a>
  <a href="https://developer.android.com/about/versions/oreo"><img src="https://img.shields.io/badge/Android-API%2026%2B-3ddc84?style=flat-square&logo=android&logoColor=white" alt="Android API 26+" /></a>
  <a href="https://www.java.com/"><img src="https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=openjdk&logoColor=white" alt="Java 17" /></a>
  <a href="https://developer.android.com/media/media3"><img src="https://img.shields.io/badge/Media3-ExoPlayer-4285f4?style=flat-square&logo=google" alt="Media3 ExoPlayer" /></a>
</p>

<table align="center">
  <tr>
    <td align="center"><strong>☕ Java</strong><br/><sub>Ứng dụng Android</sub></td>
    <td align="center"><strong>▦ XML</strong><br/><sub>Views và tài nguyên</sub></td>
    <td align="center"><strong>▶ Media3</strong><br/><sub>ExoPlayer IPTV</sub></td>
    <td align="center"><strong>⚙ Gradle</strong><br/><sub>Đóng gói APK</sub></td>
  </tr>
</table>

## Tính năng

- Phát M3U/HLS và MPEG-TS trong app bằng Media3 ExoPlayer.
- Tự nhớ kênh gần nhất, playlist và danh sách yêu thích.
- TV Guide có nhóm kênh, tìm kiếm, logo, EPG, lựa chọn audio và phụ đề nhúng.
- OSD hiển thị độ phân giải, codec, FPS, bitrate và thông tin audio.
- Nhận diện luồng 50 fps và yêu cầu đồng bộ tần số màn hình khi Android TV hỗ trợ.
- Làm mới playlist mỗi 30 phút, không ngắt phát nếu URL luồng không đổi.
- Shortcut Home cho VTV1, VTV3, VTV6, Live sự kiện và Giải Trí.
- Kiểm tra `update.json` nền và báo khi có bản mới.

## Cài đặt nhanh trên Android TV / LEAP-S1

### Qua Downloader

Mở Downloader trên TV và nhập mã:

```text
2817291
```

Mã AFTVnews tải APK qua CDN GitHub Releases.

- Short URL: https://aftv.news/2817291
- APK: https://github.com/Phu25709/norvis-tv-plus/releases/download/v0.2.27/TV-Nha-Plus-0.2.29-qr-guide.apk

### Thêm playlist

1. Mở **Norvis TV Plus** và chọn **Thêm playlist M3U**.
2. Dán đường dẫn M3U qua HTTP/HTTPS, rồi chọn **Tải danh sách**.
3. Trong khi xem, bấm **OK** để mở TV Guide; dùng lên/xuống hoặc phím số để đổi kênh.
4. Trong Guide, giữ **OK** trên kênh để thêm/bỏ yêu thích; **Back** quay lại phát.

Link mẫu có sẵn trong app: `https://tinyurl.com/vmt47`.

### Điều khiển remote

| Nút | Tác vụ |
|---|---|
| OK khi đang xem | Mở TV Guide |
| OK trên kênh | Phát kênh |
| Giữ OK trên kênh | Thêm/bỏ yêu thích |
| Lên/xuống | Chuyển kênh |
| Phím số | Dò số kênh |
| Trái/phải khi phát | Tua 10 giây nếu luồng có DVR |
| Back | Quay lại màn trước |

## Nhập playlist bằng QR trong mạng LAN

1. TV và điện thoại kết nối cùng Wi-Fi/LAN.
2. Trên Home, chọn **Nhập từ điện thoại** để hiện QR; trong TV Guide, nút **QR / Điện thoại** hiện địa chỉ pairing.
3. Quét QR hoặc nhập địa chỉ hiển thị trên TV vào trình duyệt điện thoại.
4. Gửi đường dẫn playlist. TV sẽ hỏi xác nhận trước khi tải và lưu.

Trang pairing chạy tạm trên TV và nhận nội dung qua mạng LAN. QR được tạo bằng dịch vụ QuickChart nên URL pairing (chứa địa chỉ LAN của TV) được gửi tới dịch vụ này để tạo ảnh; đường dẫn playlist được gửi trực tiếp từ điện thoại tới TV. Trình nhập hiện hỗ trợ playlist M3U; thông tin Xtream Codes chưa được chuyển thành playlist bởi importer hiện tại.

## Cập nhật ứng dụng

Sau khi player mở, app kiểm tra `update.json`. Nếu `versionCode` trên manifest mới hơn bản đang cài, app báo cho người dùng và mở link APK khi chọn **Cập nhật**. Lỗi kết nối không làm gián đoạn phát.

## Phiên bản và build

Phiên bản source/APK local mới nhất: **0.2.29**, versionCode **31**. Release công khai hiện trên GitHub: **v0.2.27**.

Yêu cầu: Android SDK 34, JDK 17, Gradle 8.9.

```powershell
gradle assembleDebug
gradle assembleRelease
```

- Application ID: `vn.hoanghoa.tvnhaplus`
- Minimum Android: API 26 (Android 8)
- Media3 ExoPlayer: 1.4.1

## Tương thích và giới hạn

- Đã kiểm tra trên Skyworth Formuler LEAP-S1, Android 14.
- 4K, 50 fps và Dolby Digital/5.1 phụ thuộc nguồn phát, mạng, decoder, HDMI và TV/receiver.
- DRM, link hết hạn hoặc nguồn cần HTTP header riêng có thể không phát.
- Playlist được lưu trong bộ nhớ riêng của app; dữ liệu playlist cá nhân không nằm trong repo.

## Giấy phép và nguồn phát

Dự án phục vụ nghiên cứu và sử dụng cá nhân. Hãy kiểm tra quyền và điều khoản của nguồn IPTV trước khi sử dụng hoặc chia sẻ.
