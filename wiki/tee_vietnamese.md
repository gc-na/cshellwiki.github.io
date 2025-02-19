# [Hệ điều hành] C Shell (csh) tee Cách sử dụng: Ghi và hiển thị đầu ra

## Tổng quan
Lệnh `tee` trong C Shell (csh) được sử dụng để đọc từ đầu vào chuẩn và ghi vào cả đầu ra chuẩn và một hoặc nhiều tệp. Điều này cho phép bạn xem dữ liệu đầu ra trên màn hình đồng thời lưu trữ nó vào tệp.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tee` như sau:
```
tee [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Ghi vào tệp ở chế độ bổ sung (append) thay vì ghi đè.
- `-i`: Bỏ qua tín hiệu ngắt (interrupt signal).

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `tee`:

1. Ghi đầu ra của lệnh `ls` vào tệp `output.txt`:
   ```csh
   ls | tee output.txt
   ```

2. Ghi đầu ra của lệnh `echo` vào tệp `log.txt` và hiển thị trên màn hình:
   ```csh
   echo "Hello, World!" | tee log.txt
   ```

3. Ghi đầu ra của lệnh `df` vào tệp `disk_usage.txt` ở chế độ bổ sung:
   ```csh
   df | tee -a disk_usage.txt
   ```

4. Ghi đầu ra của lệnh `cat` vào tệp `data.txt` và bỏ qua tín hiệu ngắt:
   ```csh
   cat file.txt | tee -i data.txt
   ```

## Mẹo
- Sử dụng tùy chọn `-a` khi bạn muốn thêm dữ liệu vào tệp mà không làm mất dữ liệu cũ.
- Kết hợp `tee` với các lệnh khác trong pipeline để dễ dàng theo dõi và lưu trữ đầu ra.
- Kiểm tra nội dung của tệp đã ghi bằng lệnh `cat` hoặc `less` để đảm bảo rằng dữ liệu đã được lưu đúng cách.