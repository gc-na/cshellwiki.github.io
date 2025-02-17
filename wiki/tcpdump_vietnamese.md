# [Linux] Bash tcpdump Cách sử dụng: Ghi lại và phân tích lưu lượng mạng

## Tổng quan
Lệnh `tcpdump` là một công cụ mạnh mẽ trong Bash dùng để ghi lại và phân tích lưu lượng mạng. Nó cho phép người dùng xem các gói dữ liệu đang được gửi và nhận qua mạng, giúp trong việc chẩn đoán sự cố và bảo mật.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tcpdump` như sau:

```bash
tcpdump [options] [arguments]
```

## Các tùy chọn phổ biến
- `-i <interface>`: Chỉ định giao diện mạng để theo dõi (ví dụ: eth0, wlan0).
- `-c <count>`: Số lượng gói tin sẽ được ghi lại trước khi dừng.
- `-w <file>`: Ghi lại lưu lượng vào một tệp tin.
- `-r <file>`: Đọc lưu lượng từ một tệp tin đã ghi.
- `-n`: Không phân giải địa chỉ IP thành tên miền.
- `-v`, `-vv`, `-vvv`: Tăng cường mức độ chi tiết của thông tin được hiển thị.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng `tcpdump`:

1. Ghi lại tất cả lưu lượng trên giao diện mạng `eth0`:
   ```bash
   tcpdump -i eth0
   ```

2. Ghi lại 10 gói tin và sau đó dừng:
   ```bash
   tcpdump -i eth0 -c 10
   ```

3. Ghi lại lưu lượng vào tệp tin `capture.pcap`:
   ```bash
   tcpdump -i eth0 -w capture.pcap
   ```

4. Đọc lưu lượng từ tệp tin `capture.pcap`:
   ```bash
   tcpdump -r capture.pcap
   ```

5. Ghi lại lưu lượng HTTP (cổng 80):
   ```bash
   tcpdump -i eth0 port 80
   ```

## Mẹo
- Sử dụng tùy chọn `-n` để tăng tốc độ ghi lại bằng cách tránh phân giải tên miền.
- Kiểm tra các giao diện mạng có sẵn bằng lệnh `tcpdump -D`.
- Thực hiện lệnh với quyền `sudo` nếu cần thiết để có quyền truy cập vào các giao diện mạng.
- Lưu trữ các tệp tin ghi lại để phân tích sau này, đặc biệt trong các tình huống bảo mật.