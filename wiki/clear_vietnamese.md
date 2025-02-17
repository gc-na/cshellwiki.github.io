# [Linux] Bash clear lệnh: Xóa màn hình terminal

## Tổng quan
Lệnh `clear` trong Bash được sử dụng để xóa nội dung hiện tại trên màn hình terminal, giúp người dùng có một không gian làm việc sạch sẽ và dễ nhìn hơn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `clear` như sau:
```
clear [options] [arguments]
```

## Tùy chọn thông dụng
- `-x`: Xóa màn hình và xóa cả lịch sử cuộn.
- `-s`: Chỉ xóa màn hình mà không làm thay đổi vị trí con trỏ.

## Ví dụ thông dụng
Dưới đây là một số ví dụ về cách sử dụng lệnh `clear`:

1. Xóa màn hình terminal:
   ```bash
   clear
   ```

2. Xóa màn hình và lịch sử cuộn:
   ```bash
   clear -x
   ```

3. Xóa màn hình mà không thay đổi vị trí con trỏ:
   ```bash
   clear -s
   ```

## Mẹo
- Sử dụng phím tắt `Ctrl + L` cũng có thể đạt được hiệu ứng tương tự như lệnh `clear`.
- Nếu bạn thường xuyên cần xóa màn hình, hãy xem xét việc tạo một alias trong file cấu hình shell của bạn, ví dụ: `alias cls='clear'` để dễ dàng sử dụng hơn.