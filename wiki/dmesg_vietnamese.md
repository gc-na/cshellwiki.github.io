# [Linux] Bash dmesg Cách sử dụng: Xem thông tin log kernel

## Tổng quan
Lệnh `dmesg` được sử dụng để hiển thị thông tin log của kernel, giúp người dùng theo dõi các sự kiện hệ thống, thông báo lỗi, và trạng thái của phần cứng. Đây là công cụ hữu ích cho việc gỡ lỗi và phân tích các vấn đề liên quan đến hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `dmesg` như sau:
```
dmesg [options] [arguments]
```

## Các tùy chọn phổ biến
- `-c`: Xóa log sau khi hiển thị.
- `-n level`: Đặt mức độ thông báo tối thiểu để hiển thị.
- `-T`: Hiển thị thời gian dạng con người (human-readable).
- `--follow`: Theo dõi log theo thời gian thực.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `dmesg`:

1. Hiển thị tất cả thông tin log kernel:
   ```bash
   dmesg
   ```

2. Hiển thị log với thời gian dạng con người:
   ```bash
   dmesg -T
   ```

3. Xóa log sau khi hiển thị:
   ```bash
   dmesg -c
   ```

4. Theo dõi log theo thời gian thực:
   ```bash
   dmesg --follow
   ```

5. Đặt mức độ thông báo tối thiểu là thông báo cảnh báo:
   ```bash
   dmesg -n 1
   ```

## Mẹo
- Sử dụng `dmesg | less` để dễ dàng cuộn qua các thông báo dài.
- Kết hợp với `grep` để tìm kiếm thông báo cụ thể, ví dụ: `dmesg | grep error`.
- Thường xuyên kiểm tra log kernel khi gặp sự cố phần cứng hoặc lỗi hệ thống để có thông tin chi tiết hơn.