# [Linux] Bash brew sử dụng: Quản lý gói phần mềm

## Overview
Lệnh `brew` là một công cụ quản lý gói phần mềm trên hệ điều hành macOS và Linux, cho phép người dùng cài đặt, cập nhật và quản lý các ứng dụng và thư viện một cách dễ dàng.

## Usage
Cú pháp cơ bản của lệnh `brew` như sau:
```bash
brew [options] [arguments]
```

## Common Options
- `install`: Cài đặt một gói phần mềm.
- `update`: Cập nhật danh sách gói phần mềm có sẵn.
- `upgrade`: Nâng cấp gói phần mềm đã cài đặt lên phiên bản mới nhất.
- `remove`: Gỡ bỏ một gói phần mềm.
- `list`: Liệt kê các gói phần mềm đã cài đặt.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `brew`:

- Cài đặt một gói phần mềm:
  ```bash
  brew install wget
  ```

- Cập nhật danh sách gói phần mềm:
  ```bash
  brew update
  ```

- Nâng cấp tất cả các gói phần mềm đã cài đặt:
  ```bash
  brew upgrade
  ```

- Gỡ bỏ một gói phần mềm:
  ```bash
  brew remove wget
  ```

- Liệt kê các gói phần mềm đã cài đặt:
  ```bash
  brew list
  ```

## Tips
- Luôn chạy `brew update` trước khi cài đặt hoặc nâng cấp để đảm bảo bạn có danh sách gói mới nhất.
- Sử dụng `brew search [package_name]` để tìm kiếm gói phần mềm trước khi cài đặt.
- Kiểm tra thông tin chi tiết về một gói bằng lệnh `brew info [package_name]`.