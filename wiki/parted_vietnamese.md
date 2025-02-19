# [Hệ điều hành] C Shell (csh) parted Cách sử dụng: Quản lý phân vùng ổ đĩa

## Tổng quan
Lệnh `parted` được sử dụng để quản lý các phân vùng trên ổ đĩa. Nó cho phép người dùng tạo, xóa, thay đổi kích thước và quản lý các phân vùng một cách dễ dàng và hiệu quả.

## Cách sử dụng
Cú pháp cơ bản của lệnh `parted` như sau:
```
parted [options] [arguments]
```

## Các tùy chọn phổ biến
- `-l`, `--list`: Hiển thị danh sách các ổ đĩa và phân vùng hiện có.
- `mkpart`: Tạo một phân vùng mới.
- `rm`: Xóa một phân vùng.
- `resizepart`: Thay đổi kích thước một phân vùng hiện có.
- `print`: Hiển thị thông tin chi tiết về các phân vùng trên ổ đĩa.

## Ví dụ phổ biến
1. **Hiển thị danh sách các ổ đĩa và phân vùng:**
   ```bash
   parted -l
   ```

2. **Tạo một phân vùng mới:**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Xóa một phân vùng:**
   ```bash
   parted /dev/sda rm 1
   ```

4. **Thay đổi kích thước một phân vùng:**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **Hiển thị thông tin chi tiết về các phân vùng:**
   ```bash
   parted /dev/sda print
   ```

## Mẹo
- Trước khi thực hiện bất kỳ thay đổi nào với phân vùng, hãy sao lưu dữ liệu quan trọng để tránh mất mát dữ liệu.
- Sử dụng lệnh `print` để kiểm tra trạng thái hiện tại của các phân vùng trước khi thực hiện các thay đổi.
- Đảm bảo rằng bạn có quyền truy cập root hoặc sử dụng `sudo` khi cần thiết để thực hiện các thao tác trên phân vùng.