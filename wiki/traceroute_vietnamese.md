# [Linux] Bash traceroute cách sử dụng: Xác định đường đi của gói tin mạng

## Tổng quan
Lệnh `traceroute` được sử dụng để theo dõi đường đi của gói tin từ máy tính của bạn đến một địa chỉ IP hoặc tên miền cụ thể. Nó giúp xác định các điểm trung gian mà gói tin đi qua, từ đó hỗ trợ trong việc phân tích hiệu suất mạng và phát hiện sự cố.

## Cách sử dụng
Cú pháp cơ bản của lệnh `traceroute` như sau:

```bash
traceroute [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-n`: Hiển thị địa chỉ IP thay vì tên miền.
- `-m <hop limit>`: Đặt giới hạn số lượng hop tối đa mà gói tin có thể đi qua.
- `-p <port>`: Chỉ định cổng để gửi gói tin.
- `-w <timeout>`: Đặt thời gian chờ cho mỗi gói tin.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `traceroute`:

1. Truy tìm đường đi đến một tên miền:
   ```bash
   traceroute example.com
   ```

2. Truy tìm đường đi đến một địa chỉ IP cụ thể:
   ```bash
   traceroute 8.8.8.8
   ```

3. Sử dụng tùy chọn `-n` để hiển thị địa chỉ IP:
   ```bash
   traceroute -n example.com
   ```

4. Đặt giới hạn số hop tối đa là 10:
   ```bash
   traceroute -m 10 example.com
   ```

5. Chỉ định cổng 80 để gửi gói tin:
   ```bash
   traceroute -p 80 example.com
   ```

## Mẹo
- Sử dụng tùy chọn `-n` nếu bạn muốn tăng tốc độ thực hiện lệnh, vì nó tránh việc phân giải tên miền.
- Kiểm tra kết nối mạng của bạn trước khi sử dụng `traceroute` để đảm bảo rằng bạn có thể gửi gói tin ra ngoài.
- Nếu bạn gặp phải thời gian chờ lâu, hãy thử tăng giá trị của tùy chọn `-w` để xem liệu có cải thiện được không.