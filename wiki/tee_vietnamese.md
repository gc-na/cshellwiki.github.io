# [Linux] Bash tee Cách sử dụng: Ghi đầu ra vào tệp và màn hình

## Tổng quan
Lệnh `tee` trong Bash được sử dụng để đọc từ đầu vào chuẩn và ghi đồng thời vào đầu ra chuẩn và một hoặc nhiều tệp. Điều này rất hữu ích khi bạn muốn xem đầu ra của một lệnh trên màn hình đồng thời lưu nó vào tệp.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tee` như sau:

```bash
tee [tùy chọn] [tệp]
```

## Tùy chọn phổ biến
- `-a` hoặc `--append`: Ghi thêm vào tệp thay vì ghi đè.
- `-i` hoặc `--ignore-interrupts`: Bỏ qua các tín hiệu ngắt.
- `--help`: Hiển thị thông tin trợ giúp về lệnh tee.
- `--version`: Hiển thị phiên bản của lệnh tee.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `tee`:

1. Ghi đầu ra của lệnh `echo` vào tệp:
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. Ghi đầu ra của lệnh `ls` vào tệp và hiển thị trên màn hình:
   ```bash
   ls -l | tee directory_list.txt
   ```

3. Ghi thêm vào tệp mà không ghi đè:
   ```bash
   echo "New line" | tee -a output.txt
   ```

4. Ghi đầu ra của một lệnh phức tạp vào nhiều tệp:
   ```bash
   ps aux | tee process_list.txt | grep bash > bash_processes.txt
   ```

## Mẹo
- Sử dụng tùy chọn `-a` để ghi thêm vào tệp mà không làm mất dữ liệu cũ.
- Kết hợp `tee` với các lệnh khác để lưu trữ đầu ra của các lệnh phức tạp.
- Hãy cẩn thận khi ghi vào tệp, vì việc không sử dụng tùy chọn `-a` sẽ ghi đè lên nội dung hiện có.