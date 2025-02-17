# [Linux] Bash parted cách sử dụng: Quản lý phân vùng ổ đĩa

## Tổng quan
Lệnh `parted` là một công cụ mạnh mẽ dùng để quản lý phân vùng trên ổ đĩa. Nó cho phép người dùng tạo, xóa, thay đổi kích thước và định dạng các phân vùng, giúp tối ưu hóa không gian lưu trữ trên hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `parted` như sau:

```
parted [options] [arguments]
```

## Các tùy chọn phổ biến
- `-l`, `--list`: Liệt kê tất cả các ổ đĩa và phân vùng hiện có.
- `mkpart`: Tạo một phân vùng mới.
- `rm`: Xóa một phân vùng.
- `resizepart`: Thay đổi kích thước một phân vùng hiện có.
- `print`: Hiển thị thông tin chi tiết về phân vùng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `parted`.

### Liệt kê các ổ đĩa và phân vùng
```bash
parted -l
```

### Tạo một phân vùng mới
```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### Xóa một phân vùng
```bash
parted /dev/sda rm 1
```

### Thay đổi kích thước một phân vùng
```bash
parted /dev/sda resizepart 1 200MiB
```

### Hiển thị thông tin phân vùng
```bash
parted /dev/sda print
```

## Mẹo
- Luôn sao lưu dữ liệu trước khi thực hiện bất kỳ thay đổi nào trên phân vùng để tránh mất mát dữ liệu.
- Sử dụng lệnh `print` để kiểm tra cấu trúc phân vùng hiện tại trước khi thực hiện các thay đổi.
- Đảm bảo rằng bạn có quyền truy cập root hoặc sử dụng `sudo` khi cần thiết để thực hiện các thao tác trên phân vùng.