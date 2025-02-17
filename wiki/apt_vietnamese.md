# [Linux] Bash apt cách sử dụng: Quản lý gói phần mềm

## Tổng quan
Lệnh `apt` (Advanced Package Tool) là một công cụ quản lý gói trên các hệ điều hành dựa trên Debian, cho phép người dùng cài đặt, nâng cấp và xóa các gói phần mềm một cách dễ dàng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `apt` như sau:
```
apt [options] [arguments]
```

## Các tùy chọn phổ biến
- `update`: Cập nhật danh sách các gói có sẵn.
- `upgrade`: Nâng cấp tất cả các gói đã cài đặt lên phiên bản mới nhất.
- `install <package>`: Cài đặt gói phần mềm cụ thể.
- `remove <package>`: Gỡ bỏ gói phần mềm cụ thể.
- `search <keyword>`: Tìm kiếm gói phần mềm theo từ khóa.
- `show <package>`: Hiển thị thông tin chi tiết về gói phần mềm.

## Ví dụ phổ biến
- Cập nhật danh sách gói:
  ```bash
  sudo apt update
  ```

- Nâng cấp tất cả các gói đã cài đặt:
  ```bash
  sudo apt upgrade
  ```

- Cài đặt gói phần mềm `curl`:
  ```bash
  sudo apt install curl
  ```

- Gỡ bỏ gói phần mềm `curl`:
  ```bash
  sudo apt remove curl
  ```

- Tìm kiếm gói phần mềm với từ khóa `vim`:
  ```bash
  apt search vim
  ```

- Hiển thị thông tin chi tiết về gói phần mềm `git`:
  ```bash
  apt show git
  ```

## Mẹo
- Luôn sử dụng `sudo` để đảm bảo bạn có quyền truy cập cần thiết khi thực hiện các thay đổi hệ thống.
- Sử dụng `apt autoremove` để gỡ bỏ các gói không còn cần thiết sau khi gỡ bỏ gói chính.
- Thực hiện `apt update` thường xuyên để đảm bảo bạn có danh sách gói mới nhất và tránh gặp phải lỗi khi cài đặt.