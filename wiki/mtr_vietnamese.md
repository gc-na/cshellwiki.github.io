# [Hệ điều hành] C Shell (csh) mtr <Sử dụng tương đương>: Kiểm tra kết nối mạng

## Tổng quan
Lệnh `mtr` kết hợp giữa chức năng của `ping` và `traceroute`, cho phép người dùng theo dõi đường đi của gói tin từ máy tính của họ đến một địa chỉ IP hoặc tên miền cụ thể. Nó cung cấp thông tin chi tiết về độ trễ và tỷ lệ mất gói tin trên từng bước của đường truyền.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mtr` như sau:
```
mtr [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-r`: Chạy trong chế độ báo cáo, xuất kết quả dưới dạng bảng.
- `-c <số>`: Chỉ định số lần gửi gói tin.
- `-i <giây>`: Đặt khoảng thời gian giữa các lần gửi gói tin.
- `-p`: Chạy trong chế độ chỉ xem, không gửi gói tin.

## Ví dụ phổ biến
1. Kiểm tra kết nối đến một địa chỉ IP:
   ```bash
   mtr 8.8.8.8
   ```

2. Chạy mtr với chế độ báo cáo và gửi 10 gói tin:
   ```bash
   mtr -r -c 10 8.8.8.8
   ```

3. Kiểm tra kết nối với khoảng thời gian 1 giây giữa các gói tin:
   ```bash
   mtr -i 1 8.8.8.8
   ```

4. Chạy mtr trong chế độ chỉ xem:
   ```bash
   mtr -p 8.8.8.8
   ```

## Mẹo
- Sử dụng tùy chọn `-r` để có được báo cáo rõ ràng và dễ đọc hơn.
- Thử nghiệm với các khoảng thời gian khác nhau bằng cách sử dụng tùy chọn `-i` để xem ảnh hưởng đến độ trễ.
- Nếu bạn chỉ muốn kiểm tra một lần mà không cần theo dõi liên tục, hãy sử dụng tùy chọn `-c` để giới hạn số lần gửi gói tin.