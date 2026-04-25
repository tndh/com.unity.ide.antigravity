# Unity Antigravity Editor Integration

Plugin tích hợp Antigravity Editor với Unity, hỗ trợ IntelliSense, debugging và tự động tạo project files.

## Tính năng

- 🔍 Tự động phát hiện Antigravity installation trên Windows, macOS và Linux
- 📝 Tạo file `.csproj` và `.sln` cho IntelliSense
- 🐛 Hỗ trợ debugging Unity projects
- ⚙️ Tự động cấu hình workspace (`.vscode/settings.json`, `launch.json`, `extensions.json`)
- 🔄 Đồng bộ project files khi có thay đổi
- 🧪 Tích hợp Unity Test Framework
- Giữ nguyên trạng thái fullscreen của Antigravity khi mở script từ Unity bằng cách tái sử dụng cửa sổ hiện tại

## Cài đặt nhanh

✅ **Antigravity có thể cùng tồn tại với Windsurf** - Không cần gỡ package cũ!

1. Mở Unity → **Window** → **Package Manager**
2. Click **"+"** → **"Add package from git URL..."**
3. Nhập: `https://github.com/tndh/com.unity.ide.antigravity.git`
4. Click **"Add"**
5. Chọn editor trong **Edit** → **Preferences** → **External Tools**

Xem [INSTALLATION.md](INSTALLATION.md) để biết thêm chi tiết.
Gặp vấn đề? Xem [TROUBLESHOOTING.md](TROUBLESHOOTING.md).

## Cập nhật từ Git trong Unity

Sau khi repository đã có commit mới, mở **Window** → **Package Manager**, chọn **Antigravity Editor**, rồi dùng nút update/refresh nếu Unity hiển thị. Nếu Unity vẫn giữ cache bản cũ, hãy remove package và add lại cùng Git URL: `https://github.com/tndh/com.unity.ide.antigravity.git`.

Nếu project vẫn khóa revision cũ, đóng Unity và xóa entry `com.unity.ide.antigravity` trong `Packages/packages-lock.json`, sau đó mở lại Unity để Package Manager resolve lại bản Git mới.

## Cấu hình

Sau khi cài đặt:
1. **Edit** → **Preferences** → **External Tools**
2. Chọn **Antigravity** trong dropdown **External Script Editor**
3. Click **"Regenerate project files"**

![Package Add](PackageImage.png)

## Yêu cầu

- Unity 2019.4 trở lên
- Antigravity Editor

## Kiểm tra phát hiện Antigravity (Windows)

Nếu Unity không tự động phát hiện Antigravity, chạy script test:

```powershell
powershell -ExecutionPolicy Bypass -File test-antigravity-detection.ps1
```

Script sẽ quét tất cả ổ đĩa và hiển thị vị trí Antigravity được tìm thấy.

## Mở file từ Unity

Khi double-click script trong Unity, package sẽ mở file trong Antigravity bằng cửa sổ project hiện tại (`--reuse-window`) và nhảy đúng dòng/cột (`-g`). Cách này tránh việc Antigravity bị launch lại hoặc thoát khỏi fullscreen/window state hiện có.

## Đóng góp

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - xem [LICENSE.md](LICENSE.md) để biết thêm chi tiết.
