# [Linux] Bash head cách sử dụng: Lấy dòng đầu tiên của tệp

## Tổng quan
Lệnh `head` trong Bash được sử dụng để hiển thị một số dòng đầu tiên của một tệp. Mặc định, lệnh này sẽ hiển thị 10 dòng đầu tiên, nhưng bạn có thể thay đổi số lượng dòng hiển thị theo nhu cầu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `head` như sau:

```
head [tùy chọn] [tệp]
```

## Tùy chọn phổ biến
- `-n [số]`: Chỉ định số dòng cần hiển thị. Ví dụ: `-n 5` sẽ hiển thị 5 dòng đầu tiên.
- `-c [số]`: Hiển thị số byte đầu tiên thay vì số dòng.
- `-q`: Không hiển thị tiêu đề tệp khi có nhiều tệp được chỉ định.
- `-v`: Luôn hiển thị tiêu đề tệp ngay cả khi chỉ có một tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `head`:

1. Hiển thị 10 dòng đầu tiên của tệp `example.txt`:
   ```bash
   head example.txt
   ```

2. Hiển thị 5 dòng đầu tiên của tệp `example.txt`:
   ```bash
   head -n 5 example.txt
   ```

3. Hiển thị 20 byte đầu tiên của tệp `example.txt`:
   ```bash
   head -c 20 example.txt
   ```

4. Hiển thị 10 dòng đầu tiên của nhiều tệp:
   ```bash
   head file1.txt file2.txt
   ```

5. Hiển thị tiêu đề tệp ngay cả khi chỉ có một tệp:
   ```bash
   head -v example.txt
   ```

## Mẹo
- Sử dụng `head` kết hợp với các lệnh khác như `grep` hoặc `sort` để lọc và hiển thị thông tin cần thiết.
- Khi làm việc với các tệp lớn, `head` là một công cụ hữu ích để xem nhanh nội dung mà không cần mở toàn bộ tệp.
- Hãy nhớ rằng bạn có thể thay đổi số dòng hiển thị bằng cách sử dụng tùy chọn `-n`, điều này rất hữu ích khi bạn chỉ cần một cái nhìn tổng quan về dữ liệu.