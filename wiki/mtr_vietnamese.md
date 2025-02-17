# [Linux] Bash mtr Cách sử dụng: Kiểm tra kết nối mạng

## Tổng quan
Lệnh `mtr` (My Traceroute) là một công cụ kết hợp giữa `ping` và `traceroute`, cho phép người dùng theo dõi đường đi của gói tin từ máy tính đến một địa chỉ IP hoặc tên miền cụ thể. Nó cung cấp thông tin chi tiết về độ trễ và tỷ lệ mất gói tin tại từng nút mạng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mtr` như sau:

```
mtr [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-r`: Chạy trong chế độ báo cáo, hiển thị kết quả sau khi hoàn tất.
- `-c <số>`: Chỉ định số lần gửi gói tin (mặc định là vô hạn).
- `-i <giây>`: Thay đổi khoảng thời gian giữa các lần gửi gói tin.
- `-p`: Chạy trong chế độ chỉ hiển thị các nút mà không thực hiện kiểm tra.

## Ví dụ phổ biến
1. Kiểm tra kết nối đến một địa chỉ IP hoặc tên miền:
   ```bash
   mtr google.com
   ```

2. Chạy mtr trong chế độ báo cáo và gửi 10 gói tin:
   ```bash
   mtr -r -c 10 google.com
   ```

3. Thay đổi khoảng thời gian gửi gói tin thành 1 giây:
   ```bash
   mtr -i 1 google.com
   ```

4. Chạy mtr mà không thực hiện kiểm tra, chỉ hiển thị các nút:
   ```bash
   mtr -p google.com
   ```

## Mẹo
- Sử dụng tùy chọn `-r` để có kết quả rõ ràng hơn khi bạn chỉ muốn xem kết quả cuối cùng mà không cần theo dõi trực tiếp.
- Nếu bạn muốn theo dõi một kết nối trong thời gian dài, hãy kết hợp `-c` với một số lớn để có được thông tin chính xác hơn.
- Kiểm tra kết nối đến nhiều địa chỉ khác nhau để xác định xem vấn đề nằm ở đâu trong mạng của bạn.