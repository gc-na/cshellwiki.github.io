# [Linux] Bash journalctl Cách sử dụng: Xem nhật ký hệ thống

## Tổng quan
Lệnh `journalctl` được sử dụng để truy cập và xem nhật ký hệ thống trên các hệ thống Linux sử dụng systemd. Nó cho phép người dùng xem các thông tin ghi lại bởi các dịch vụ và ứng dụng, giúp theo dõi và khắc phục sự cố.

## Cách sử dụng
Cú pháp cơ bản của lệnh `journalctl` như sau:
```
journalctl [options] [arguments]
```

## Các tùy chọn phổ biến
- `-b`: Hiển thị nhật ký từ lần khởi động gần nhất.
- `-f`: Theo dõi nhật ký theo thời gian thực (tương tự như lệnh `tail -f`).
- `--since "time"`: Hiển thị nhật ký từ một thời điểm cụ thể.
- `--until "time"`: Hiển thị nhật ký cho đến một thời điểm cụ thể.
- `-u <service>`: Hiển thị nhật ký cho một dịch vụ cụ thể.

## Ví dụ thường gặp
- Hiển thị tất cả nhật ký:
  ```bash
  journalctl
  ```

- Hiển thị nhật ký từ lần khởi động gần nhất:
  ```bash
  journalctl -b
  ```

- Theo dõi nhật ký theo thời gian thực:
  ```bash
  journalctl -f
  ```

- Hiển thị nhật ký từ một thời điểm cụ thể:
  ```bash
  journalctl --since "2023-10-01 10:00:00"
  ```

- Hiển thị nhật ký cho một dịch vụ cụ thể:
  ```bash
  journalctl -u ssh.service
  ```

## Mẹo
- Sử dụng `-n <number>` để chỉ định số lượng dòng nhật ký muốn hiển thị, ví dụ: `journalctl -n 100` để xem 100 dòng cuối cùng.
- Kết hợp các tùy chọn để lọc nhật ký hiệu quả hơn, chẳng hạn như `journalctl -u nginx.service --since "1 hour ago"`.
- Thường xuyên kiểm tra nhật ký để phát hiện sớm các vấn đề tiềm ẩn trong hệ thống.