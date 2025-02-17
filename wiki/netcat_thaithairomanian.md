# [Linux] Bash netcat sử dụng: Giao tiếp mạng đơn giản

## Overview
Netcat, thường được gọi là "nc", là một công cụ mạnh mẽ trong Bash cho phép người dùng thực hiện các kết nối mạng TCP hoặc UDP. Nó có thể được sử dụng để gửi và nhận dữ liệu giữa các máy tính, kiểm tra kết nối mạng, và thậm chí làm máy chủ hoặc khách hàng cho các ứng dụng mạng.

## Usage
Cú pháp cơ bản của lệnh netcat như sau:
```bash
netcat [options] [arguments]
```

## Common Options
- `-l`: Chế độ lắng nghe, cho phép netcat hoạt động như một máy chủ.
- `-p [port]`: Chỉ định cổng mà netcat sẽ sử dụng.
- `-u`: Sử dụng giao thức UDP thay vì TCP.
- `-v`: Chế độ chi tiết, hiển thị thông tin thêm về kết nối.
- `-w [seconds]`: Thời gian chờ trước khi ngắt kết nối.

## Common Examples
1. **Lắng nghe trên cổng 1234**:
   ```bash
   netcat -l -p 1234
   ```
   Lệnh này sẽ khiến netcat lắng nghe trên cổng 1234, chờ kết nối từ khách hàng.

2. **Kết nối đến máy chủ trên cổng 80**:
   ```bash
   netcat example.com 80
   ```
   Lệnh này sẽ kết nối đến máy chủ `example.com` trên cổng 80, thường được sử dụng cho HTTP.

3. **Gửi một tệp tin**:
   ```bash
   netcat -l -p 1234 > received_file.txt
   ```
   Trên máy chủ, lệnh này sẽ lưu dữ liệu nhận được vào tệp `received_file.txt`. Trên máy khách, bạn có thể gửi tệp như sau:
   ```bash
   netcat example.com 1234 < file_to_send.txt
   ```

4. **Kiểm tra cổng mở**:
   ```bash
   netcat -z -v example.com 80
   ```
   Lệnh này sẽ kiểm tra xem cổng 80 trên `example.com` có mở hay không mà không gửi dữ liệu.

## Tips
- Sử dụng chế độ lắng nghe với `-l` để tạo một máy chủ tạm thời cho việc thử nghiệm.
- Kết hợp với các lệnh khác như `grep` hoặc `awk` để xử lý dữ liệu nhận được.
- Luôn kiểm tra cổng mở trên máy chủ trước khi kết nối để đảm bảo rằng không có tường lửa chặn kết nối.