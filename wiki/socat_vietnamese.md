# [Linux] Bash socat: Giao tiếp giữa các dòng dữ liệu

## Overview
`socat` là một công cụ mạnh mẽ trong Bash, cho phép bạn thiết lập các kết nối giữa các dòng dữ liệu. Nó có thể được sử dụng để chuyển tiếp dữ liệu giữa các socket, tệp, hoặc các thiết bị khác nhau, giúp tạo ra các kênh giao tiếp linh hoạt.

## Usage
Cú pháp cơ bản của lệnh `socat` như sau:

```bash
socat [options] [arguments]
```

## Common Options
- `-u`: Chạy trong chế độ không đồng bộ (unidirectional).
- `-v`: Hiển thị thông tin chi tiết về dữ liệu đang được truyền.
- `TCP:<host>:<port>`: Kết nối đến một máy chủ qua giao thức TCP.
- `UDP:<host>:<port>`: Kết nối đến một máy chủ qua giao thức UDP.
- `FILE:<filename>`: Sử dụng tệp như một nguồn hoặc đích dữ liệu.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng `socat`:

1. **Kết nối đến một máy chủ TCP:**
   ```bash
   socat - TCP:example.com:80
   ```

2. **Chuyển tiếp một cổng TCP đến một cổng khác:**
   ```bash
   socat TCP-LISTEN:8080,fork TCP:localhost:80
   ```

3. **Ghi dữ liệu vào một tệp từ một socket:**
   ```bash
   socat FILE:output.txt -
   ```

4. **Chuyển tiếp dữ liệu giữa hai cổng UDP:**
   ```bash
   socat UDP-LISTEN:1234,fork UDP:localhost:5678
   ```

## Tips
- Sử dụng tùy chọn `-v` để theo dõi dữ liệu đang được truyền, điều này rất hữu ích trong quá trình gỡ lỗi.
- Khi làm việc với các kết nối mạng, hãy đảm bảo rằng các cổng bạn sử dụng không bị chặn bởi tường lửa.
- Thử nghiệm với các tùy chọn khác nhau để tìm ra cách sử dụng phù hợp nhất cho nhu cầu của bạn.