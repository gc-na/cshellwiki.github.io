# [Hệ điều hành Linux] C Shell (csh) journalctl Sử dụng: Xem nhật ký hệ thống

## Tổng quan
Lệnh `journalctl` được sử dụng để truy cập và hiển thị nhật ký của hệ thống trên các hệ điều hành sử dụng systemd. Nó cho phép người dùng xem các thông tin chi tiết về các dịch vụ, lỗi và các sự kiện khác xảy ra trong hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `journalctl` như sau:
```
journalctl [options] [arguments]
```

## Các tùy chọn phổ biến
- `-b`: Hiển thị nhật ký từ lần khởi động gần nhất.
- `-f`: Theo dõi nhật ký theo thời gian thực (tương tự như lệnh `tail -f`).
- `--since`: Hiển thị nhật ký từ một thời điểm cụ thể.
- `--until`: Hiển thị nhật ký cho đến một thời điểm cụ thể.
- `-p`: Lọc nhật ký theo mức độ ưu tiên (ví dụ: `-p err` chỉ hiển thị lỗi).

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

- Hiển thị nhật ký lỗi:
  ```bash
  journalctl -p err
  ```

## Mẹo
- Sử dụng `-n` để chỉ định số lượng dòng nhật ký bạn muốn hiển thị, ví dụ: `journalctl -n 100` để xem 100 dòng cuối cùng.
- Kết hợp các tùy chọn để có kết quả chính xác hơn, ví dụ: `journalctl -b -p warning` để xem các cảnh báo từ lần khởi động gần nhất.
- Lưu ý rằng bạn có thể cần quyền quản trị (root) để xem một số nhật ký.