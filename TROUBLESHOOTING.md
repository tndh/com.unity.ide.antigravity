# Khắc phục sự cố

## ✅ Antigravity và Windsurf có thể cùng tồn tại

Package Antigravity được thiết kế để **không xung đột** với Windsurf. Bạn có thể cài đặt cả hai và chuyển đổi tự do.

Nếu bạn vẫn gặp lỗi GUID conflict, có thể bạn đang dùng phiên bản cũ của package. Hãy cập nhật lên phiên bản mới nhất.

## Cập nhật package Antigravity

### Từ Git URL

1. Mở **Window** → **Package Manager**
2. Tìm package **"Antigravity Editor"**
3. Click vào package đó
4. Nếu có nút **"Update"**, click để cập nhật
5. Hoặc gỡ và cài lại từ Git URL

### Kiểm tra phiên bản

Đảm bảo bạn đang dùng phiên bản 1.0.0 trở lên, phiên bản này đã có GUID độc lập.

## Antigravity không được phát hiện

**Plugin tự động tìm kiếm Antigravity ở các vị trí sau:**

### Windows
- `%LOCALAPPDATA%\Programs\Antigravity\Antigravity.exe`
- `C:\Program Files\Antigravity\Antigravity.exe`
- `C:\Program Files (x86)\Antigravity\Antigravity.exe`
- `D:\Program Files\Antigravity\Antigravity.exe`
- `E:\Program Files\Antigravity\Antigravity.exe`
- Và tất cả các ổ đĩa cố định khác

Kiểm tra bằng lệnh:
```cmd
dir "%LOCALAPPDATA%\Programs\Antigravity\Antigravity.exe"
dir "C:\Program Files\Antigravity\Antigravity.exe"
dir "D:\Program Files\Antigravity\Antigravity.exe"
```

### macOS
- `/Applications/Antigravity.app`

Kiểm tra bằng lệnh:
```bash
ls -la /Applications/Antigravity.app
```

### Linux
- `/usr/bin/antigravity`
- `/bin/antigravity`
- `/usr/local/bin/antigravity`

Kiểm tra bằng lệnh:
```bash
which antigravity
```

**Giải pháp nếu không tự động phát hiện:**

1. Đảm bảo Antigravity đã được cài đặt đúng
2. Trong Unity: **Edit** → **Preferences** → **External Tools**
3. Click nút **"Browse..."** bên cạnh **External Script Editor**
4. Chọn file `Antigravity.exe` thủ công (ví dụ: `D:\Program Files\Antigravity\Antigravity.exe`)
5. Unity sẽ nhớ đường dẫn này cho lần sau

**Lưu ý:** Plugin tự động quét tất cả ổ đĩa cố định, nhưng nếu Antigravity ở vị trí đặc biệt, bạn cần chọn thủ công.

## IntelliSense không hoạt động

1. Trong Unity: **Edit** → **Preferences** → **External Tools**
2. Đảm bảo **Antigravity** được chọn làm External Script Editor
3. Click **"Regenerate project files"**
4. Đóng và mở lại Antigravity
5. Trong Antigravity, mở Command Palette (Ctrl+Shift+P / Cmd+Shift+P)
6. Chạy lệnh: **"Developer: Reload Window"**

## Project files không được tạo

1. Kiểm tra quyền ghi file trong thư mục project
2. Xóa các file `.csproj` và `.sln` cũ
3. Trong Unity: **Edit** → **Preferences** → **External Tools**
4. Click **"Regenerate project files"**

## Debugging không hoạt động

1. Đảm bảo extension Unity cho Antigravity đã được cài đặt
2. Kiểm tra file `.vscode/launch.json` đã được tạo
3. Trong Antigravity, mở Debug panel (Ctrl+Shift+D / Cmd+Shift+D)
4. Chọn configuration **"Attach to Unity"**
5. Nhấn F5 để bắt đầu debugging

## Liên hệ hỗ trợ

Nếu vẫn gặp vấn đề, vui lòng:
1. Mở issue trên GitHub repository
2. Cung cấp thông tin:
   - Phiên bản Unity
   - Hệ điều hành
   - Phiên bản Antigravity
   - Log lỗi đầy đủ từ Unity Console
