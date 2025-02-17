# [Linux] Bash hostnamectl Cách sử dụng: Quản lý tên máy chủ

## Tổng quan
Lệnh `hostnamectl` được sử dụng để quản lý và thay đổi tên máy chủ của hệ thống Linux. Nó cho phép người dùng xem và thiết lập tên máy chủ tĩnh, tên máy chủ tạm thời cũng như thông tin về hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `hostnamectl` như sau:
```
hostnamectl [options] [arguments]
```

## Các tùy chọn phổ biến
- `set-hostname`: Đặt tên máy chủ mới.
- `status`: Hiển thị trạng thái hiện tại của tên máy chủ và thông tin hệ thống.
- `set-icon-name`: Đặt tên biểu tượng cho máy chủ.
- `set-chassis`: Đặt loại khung cho máy chủ (ví dụ: desktop, laptop, server).

## Ví dụ phổ biến
1. **Xem thông tin tên máy chủ hiện tại:**
   ```bash
   hostnamectl status
   ```

2. **Đặt tên máy chủ mới:**
   ```bash
   sudo hostnamectl set-hostname ten-may-chu-moi
   ```

3. **Đặt tên biểu tượng cho máy chủ:**
   ```bash
   sudo hostnamectl set-icon-name my-icon
   ```

4. **Đặt loại khung cho máy chủ:**
   ```bash
   sudo hostnamectl set-chassis server
   ```

## Mẹo
- Luôn sử dụng quyền `sudo` khi thay đổi tên máy chủ để đảm bảo bạn có quyền truy cập cần thiết.
- Sau khi thay đổi tên máy chủ, hãy khởi động lại hệ thống hoặc dịch vụ liên quan để áp dụng thay đổi.
- Kiểm tra lại tên máy chủ sau khi thay đổi để xác nhận rằng nó đã được cập nhật thành công.