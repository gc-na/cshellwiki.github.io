# [Linux] Bash date cách sử dụng: Lấy và định dạng thời gian hiện tại

## Tổng quan
Lệnh `date` trong Bash được sử dụng để hiển thị và định dạng thời gian hiện tại của hệ thống. Nó cho phép người dùng xem thời gian theo nhiều định dạng khác nhau và có thể được sử dụng trong các kịch bản tự động hóa.

## Cách sử dụng
Cú pháp cơ bản của lệnh `date` như sau:
```
date [options] [arguments]
```

## Các tùy chọn phổ biến
- `+FORMAT`: Định dạng đầu ra theo chuỗi FORMAT mà người dùng cung cấp.
- `-u`: Hiển thị thời gian theo giờ UTC (Thời gian phối hợp quốc tế).
- `-d STRING`: Hiển thị thời gian cho một chuỗi thời gian cụ thể.
- `-R`: Hiển thị thời gian theo định dạng RFC 2822.

## Ví dụ phổ biến
- Hiển thị thời gian hiện tại:
  ```bash
  date
  ```

- Hiển thị thời gian theo định dạng cụ thể (ngày-tháng-năm):
  ```bash
  date +"%d-%m-%Y"
  ```

- Hiển thị thời gian UTC:
  ```bash
  date -u
  ```

- Hiển thị thời gian cho một chuỗi thời gian cụ thể:
  ```bash
  date -d "next Friday"
  ```

- Hiển thị thời gian theo định dạng RFC 2822:
  ```bash
  date -R
  ```

## Mẹo
- Sử dụng `date +"%T"` để chỉ hiển thị giờ, phút và giây.
- Bạn có thể lưu kết quả của lệnh `date` vào một biến để sử dụng sau này trong kịch bản:
  ```bash
  current_date=$(date)
  echo "Thời gian hiện tại là: $current_date"
  ```
- Để tạo một tệp nhật ký với thời gian hiện tại trong tên tệp, bạn có thể sử dụng:
  ```bash
  touch "logfile_$(date +%Y%m%d_%H%M%S).txt"
  ```