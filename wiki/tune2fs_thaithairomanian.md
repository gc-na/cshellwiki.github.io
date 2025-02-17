# [Linux] Bash tune2fs sử dụng: Quản lý hệ thống tập tin ext2/ext3/ext4

## Overview
Lệnh `tune2fs` được sử dụng để điều chỉnh các tham số của hệ thống tập tin ext2, ext3 và ext4 trên Linux. Nó cho phép người dùng thay đổi các thuộc tính của hệ thống tập tin mà không cần phải định dạng lại hoặc khởi động lại hệ thống.

## Usage
Cú pháp cơ bản của lệnh `tune2fs` như sau:
```
tune2fs [options] [arguments]
```

## Common Options
- `-c <max-mount-count>`: Đặt số lần tối đa mà hệ thống tập tin có thể được gắn trước khi yêu cầu kiểm tra.
- `-i <interval>`: Đặt khoảng thời gian tối đa giữa các lần kiểm tra hệ thống tập tin.
- `-m <reserved-blocks>`: Đặt tỷ lệ phần trăm không gian dự trữ cho người dùng root.
- `-O <feature>`: Kích hoạt các tính năng mới cho hệ thống tập tin.
- `-L <label>`: Đặt nhãn cho hệ thống tập tin.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `tune2fs`:

1. **Kiểm tra số lần gắn tối đa**:
   ```bash
   tune2fs -l /dev/sda1 | grep 'Maximum mount count'
   ```

2. **Đặt số lần gắn tối đa là 20**:
   ```bash
   sudo tune2fs -c 20 /dev/sda1
   ```

3. **Kích hoạt tính năng `dir_index`**:
   ```bash
   sudo tune2fs -O dir_index /dev/sda1
   ```

4. **Đặt nhãn cho hệ thống tập tin**:
   ```bash
   sudo tune2fs -L MyLabel /dev/sda1
   ```

5. **Đặt khoảng thời gian kiểm tra là 30 ngày**:
   ```bash
   sudo tune2fs -i 30d /dev/sda1
   ```

## Tips
- Trước khi thực hiện bất kỳ thay đổi nào với `tune2fs`, hãy sao lưu dữ liệu quan trọng để tránh mất mát.
- Sử dụng lệnh `tune2fs -l` để xem thông tin chi tiết về hệ thống tập tin trước khi thực hiện các thay đổi.
- Hãy cẩn thận khi thay đổi các tham số, vì việc cấu hình sai có thể dẫn đến mất dữ liệu hoặc sự cố hệ thống.