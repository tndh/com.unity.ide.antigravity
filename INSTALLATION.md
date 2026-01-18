# Hướng dẫn cài đặt Antigravity Editor cho Unity

## ℹ️ Lưu ý

Package Antigravity có thể **cùng tồn tại** với package Windsurf (`com.unity.ide.windsurf`) mà không xung đột. Bạn có thể cài đặt cả hai và chuyển đổi giữa chúng trong Unity Preferences.

## Yêu cầu
- Unity 2019.4 trở lên
- Antigravity Editor đã được cài đặt trên máy tính

## Cài đặt từ Git URL

1. Mở Unity Editor
2. Vào **Window** → **Package Manager**
3. Click nút **"+"** ở góc trên bên trái
4. Chọn **"Add package from git URL..."**
5. Nhập URL: `https://github.com/tndh/com.unity.ide.antigravity.git`
6. Click **"Add"**
7. Đợi Unity tải và cài đặt package

## Cài đặt từ Local

1. Clone repository này về máy
2. Mở Unity Editor
3. Vào **Window** → **Package Manager**
4. Click nút **"+"** ở góc trên bên trái
5. Chọn **"Add package from disk..."**
6. Chọn file `package.json` trong thư mục đã clone

## Cấu hình

1. Sau khi cài đặt, vào **Edit** → **Preferences** (Windows/Linux) hoặc **Unity** → **Preferences** (macOS)
2. Chọn **External Tools**
3. Trong dropdown **External Script Editor**, chọn **Antigravity**
4. Click **"Regenerate project files"** nếu cần

## Sử dụng

- Double-click vào bất kỳ script C# nào trong Unity để mở trong Antigravity
- Antigravity sẽ tự động mở với IntelliSense và debugging support
- File `.vscode/` sẽ được tạo tự động với cấu hình phù hợp

## Gỡ lỗi

Nếu Antigravity không được phát hiện tự động:
- Đảm bảo Antigravity đã được cài đặt đúng cách
- Trên Windows: Kiểm tra `%LOCALAPPDATA%\Programs\Antigravity\` hoặc `C:\Program Files\Antigravity\`
- Trên macOS: Kiểm tra `/Applications/Antigravity.app`
- Trên Linux: Kiểm tra `/usr/bin/antigravity`, `/bin/antigravity`, hoặc `/usr/local/bin/antigravity`

## Tính năng

- ✅ Tự động phát hiện Antigravity installation
- ✅ Tạo file .csproj cho IntelliSense
- ✅ Hỗ trợ debugging Unity
- ✅ Tự động cấu hình workspace
- ✅ Hỗ trợ Windows, macOS, Linux
- ✅ Tích hợp với Unity Test Framework
