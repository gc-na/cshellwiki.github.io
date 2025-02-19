# [Hệ điều hành] C Shell (csh) head <Sử dụng tương đương>: Lấy một số dòng đầu tiên của tệp

## Tổng quan
Lệnh `head` trong C Shell (csh) được sử dụng để hiển thị một số dòng đầu tiên của một tệp. Đây là một công cụ hữu ích khi bạn chỉ muốn xem nội dung ban đầu của tệp mà không cần mở toàn bộ.

## Cú pháp
Cú pháp cơ bản của lệnh `head` như sau:

```
head [options] [arguments]
```

## Tùy chọn phổ biến
- `-n [số]`: Chỉ định số dòng đầu tiên cần hiển thị. Mặc định là 10 dòng.
- `-c [số]`: Hiển thị số byte đầu tiên thay vì số dòng.
- `-q`: Không hiển thị tiêu đề tệp khi có nhiều tệp được chỉ định.
- `-v`: Luôn hiển thị tiêu đề tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `head`:

1. Hiển thị 10 dòng đầu tiên của tệp `example.txt`:
   ```csh
   head example.txt
   ```

2. Hiển thị 5 dòng đầu tiên của tệp `data.txt`:
   ```csh
   head -n 5 data.txt
   ```

3. Hiển thị 20 byte đầu tiên của tệp `log.txt`:
   ```csh
   head -c 20 log.txt
   ```

4. Hiển thị 10 dòng đầu tiên của nhiều tệp và không hiển thị tiêu đề:
   ```csh
   head -q file1.txt file2.txt
   ```

5. Hiển thị tiêu đề tệp và 10 dòng đầu tiên của tệp `report.txt`:
   ```csh
   head -v report.txt
   ```

## Mẹo
- Sử dụng tùy chọn `-n` để điều chỉnh số lượng dòng bạn muốn xem, điều này rất hữu ích khi làm việc với các tệp lớn.
- Kết hợp lệnh `head` với các lệnh khác như `grep` để lọc nội dung trước khi hiển thị.
- Bạn có thể sử dụng `head` trong các kịch bản tự động hóa để kiểm tra nhanh nội dung của tệp mà không cần mở toàn bộ.