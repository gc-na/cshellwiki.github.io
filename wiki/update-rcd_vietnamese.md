# [Linux] Bash update-rc.d: Quản lý các dịch vụ khởi động

## Overview
Lệnh `update-rc.d` được sử dụng để thêm, xóa hoặc cập nhật các dịch vụ trong hệ thống khởi động của Linux. Nó cho phép người dùng quản lý cách mà các dịch vụ được khởi động hoặc dừng trong quá trình khởi động của hệ thống.

## Usage
Cú pháp cơ bản của lệnh `update-rc.d` như sau:
```
update-rc.d [options] [arguments]
```

## Common Options
- `defaults`: Thêm các liên kết khởi động mặc định cho dịch vụ.
- `remove`: Xóa dịch vụ khỏi các liên kết khởi động.
- `enable`: Kích hoạt dịch vụ để nó khởi động cùng với hệ thống.
- `disable`: Vô hiệu hóa dịch vụ để nó không khởi động cùng với hệ thống.

## Common Examples
- **Thêm dịch vụ với các liên kết khởi động mặc định:**
  ```bash
  sudo update-rc.d myservice defaults
  ```

- **Xóa dịch vụ khỏi các liên kết khởi động:**
  ```bash
  sudo update-rc.d myservice remove
  ```

- **Kích hoạt dịch vụ:**
  ```bash
  sudo update-rc.d myservice enable
  ```

- **Vô hiệu hóa dịch vụ:**
  ```bash
  sudo update-rc.d myservice disable
  ```

## Tips
- Luôn kiểm tra trạng thái của dịch vụ sau khi thực hiện các thay đổi để đảm bảo rằng nó hoạt động như mong muốn.
- Sử dụng `update-rc.d` với quyền `sudo` để đảm bảo bạn có quyền thực hiện các thay đổi cần thiết.
- Đọc tài liệu của dịch vụ cụ thể để biết thêm thông tin về cách cấu hình và quản lý dịch vụ đó.