# [macOS] Bash brew cách sử dụng: Quản lý gói phần mềm

## Tổng quan
Lệnh `brew` là một công cụ quản lý gói phần mềm trên macOS, cho phép người dùng cài đặt, cập nhật và quản lý các ứng dụng và thư viện một cách dễ dàng thông qua dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `brew` như sau:
```bash
brew [options] [arguments]
```

## Các tùy chọn phổ biến
- `install`: Cài đặt một gói phần mềm.
- `uninstall`: Gỡ bỏ một gói phần mềm.
- `update`: Cập nhật danh sách gói phần mềm.
- `upgrade`: Nâng cấp tất cả các gói phần mềm đã cài đặt.
- `list`: Liệt kê tất cả các gói phần mềm đã cài đặt.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `brew`:

### Cài đặt một gói phần mềm
```bash
brew install wget
```

### Gỡ bỏ một gói phần mềm
```bash
brew uninstall wget
```

### Cập nhật danh sách gói phần mềm
```bash
brew update
```

### Nâng cấp tất cả các gói phần mềm
```bash
brew upgrade
```

### Liệt kê các gói phần mềm đã cài đặt
```bash
brew list
```

## Mẹo
- Luôn chạy `brew update` trước khi cài đặt hoặc nâng cấp để đảm bảo bạn có danh sách gói mới nhất.
- Sử dụng `brew search [tên_gói]` để tìm kiếm các gói phần mềm có sẵn.
- Kiểm tra thông tin chi tiết về một gói phần mềm bằng cách sử dụng `brew info [tên_gói]`.