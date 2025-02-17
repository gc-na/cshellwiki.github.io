# [Linux] Bash sleep cách sử dụng: Tạm dừng thực thi trong một khoảng thời gian

## Tổng quan
Lệnh `sleep` trong Bash được sử dụng để tạm dừng thực thi của một script hoặc lệnh trong một khoảng thời gian nhất định. Điều này hữu ích khi bạn cần tạo ra khoảng thời gian chờ giữa các lệnh hoặc để trì hoãn một hành động nào đó.

## Cách sử dụng
Cú pháp cơ bản của lệnh `sleep` như sau:

```bash
sleep [tùy chọn] [thời gian]
```

## Tùy chọn phổ biến
- `-s`: Tạm dừng trong giây (mặc định).
- `-m`: Tạm dừng trong phút.
- `-h`: Tạm dừng trong giờ.
- `-d`: Tạm dừng trong ngày.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sleep`:

1. Tạm dừng trong 5 giây:
   ```bash
   sleep 5
   ```

2. Tạm dừng trong 2 phút:
   ```bash
   sleep 2m
   ```

3. Tạm dừng trong 1 giờ:
   ```bash
   sleep 1h
   ```

4. Sử dụng `sleep` trong một script để trì hoãn giữa các lệnh:
   ```bash
   echo "Bắt đầu..."
   sleep 3
   echo "Kết thúc sau 3 giây."
   ```

## Mẹo
- Sử dụng `sleep` để tạo khoảng thời gian chờ giữa các lệnh trong script, giúp dễ dàng theo dõi quá trình thực thi.
- Kết hợp `sleep` với các lệnh khác trong một vòng lặp để thực hiện các tác vụ định kỳ.
- Tránh sử dụng `sleep` quá lâu trong các script quan trọng, vì nó có thể làm chậm quá trình thực thi.