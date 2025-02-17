# [Linux] Bash resize2fs Cách sử dụng: Thay đổi kích thước hệ thống tập tin ext2/ext3/ext4

## Tổng quan
Lệnh `resize2fs` được sử dụng để thay đổi kích thước của hệ thống tập tin ext2, ext3 hoặc ext4. Lệnh này cho phép người dùng mở rộng hoặc thu nhỏ kích thước của hệ thống tập tin mà không làm mất dữ liệu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `resize2fs` như sau:

```
resize2fs [tùy chọn] [đối số]
```

## Tùy chọn thông dụng
- `-f`: Bắt buộc thực hiện thay đổi kích thước ngay cả khi hệ thống tập tin không cần thiết.
- `-p`: Hiển thị tiến trình khi thay đổi kích thước.
- `-s`: Chỉ thay đổi kích thước xuống (thu nhỏ) mà không mở rộng.
- `-M`: Thay đổi kích thước hệ thống tập tin xuống mức tối thiểu.

## Ví dụ thông dụng
Dưới đây là một số ví dụ về cách sử dụng lệnh `resize2fs`:

1. **Mở rộng hệ thống tập tin**:
   ```bash
   resize2fs /dev/sda1
   ```

2. **Thay đổi kích thước xuống một kích thước cụ thể**:
   ```bash
   resize2fs /dev/sda1 20G
   ```

3. **Hiển thị tiến trình khi thay đổi kích thước**:
   ```bash
   resize2fs -p /dev/sda1
   ```

4. **Thay đổi kích thước xuống mức tối thiểu**:
   ```bash
   resize2fs -M /dev/sda1
   ```

## Mẹo
- Trước khi thay đổi kích thước hệ thống tập tin, hãy luôn sao lưu dữ liệu quan trọng để tránh mất mát.
- Đảm bảo rằng hệ thống tập tin không đang được sử dụng (không có quá trình nào đang truy cập) khi thực hiện lệnh `resize2fs`.
- Kiểm tra tình trạng của hệ thống tập tin bằng lệnh `e2fsck` trước khi thay đổi kích thước để đảm bảo không có lỗi nào.