# [Linux] Bash cal <Sử dụng tương đương>: Hiển thị lịch

## Tổng quan
Lệnh `cal` trong Bash được sử dụng để hiển thị lịch tháng hoặc năm. Nó cho phép người dùng xem lịch một cách nhanh chóng trên dòng lệnh, giúp dễ dàng theo dõi ngày tháng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `cal` như sau:
```
cal [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `-m`: Hiển thị tháng hiện tại.
- `-y`: Hiển thị toàn bộ lịch năm hiện tại.
- `-3`: Hiển thị lịch của tháng trước, tháng hiện tại và tháng tiếp theo.
- `-j`: Hiển thị số ngày trong năm (Julian days).

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `cal`:

1. Hiển thị lịch tháng hiện tại:
   ```bash
   cal
   ```

2. Hiển thị lịch của tháng 12 năm 2023:
   ```bash
   cal 12 2023
   ```

3. Hiển thị lịch của năm 2023:
   ```bash
   cal -y 2023
   ```

4. Hiển thị lịch của tháng trước, tháng hiện tại và tháng tiếp theo:
   ```bash
   cal -3
   ```

5. Hiển thị lịch tháng hiện tại với số ngày trong năm:
   ```bash
   cal -j
   ```

## Mẹo
- Bạn có thể kết hợp các tùy chọn để tùy chỉnh hiển thị lịch theo nhu cầu của mình.
- Sử dụng lệnh `man cal` để xem thêm thông tin chi tiết về các tùy chọn và cách sử dụng của lệnh này.
- Hãy thử sử dụng `cal` trong các script tự động để dễ dàng theo dõi các ngày quan trọng trong lịch.