# [Linux] Bash basename Cách sử dụng: Lấy tên tệp từ đường dẫn

## Tổng quan
Lệnh `basename` trong Bash được sử dụng để lấy tên tệp từ một đường dẫn đầy đủ. Nó loại bỏ tất cả các phần trước tên tệp, chỉ để lại tên tệp và phần mở rộng (nếu có).

## Cách sử dụng
Cú pháp cơ bản của lệnh `basename` như sau:
```
basename [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-a`: Chấp nhận nhiều đối số và trả về tên tệp cho từng đối số.
- `-s`: Xóa phần mở rộng chỉ định từ tên tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `basename`:

1. Lấy tên tệp từ đường dẫn:
   ```bash
   basename /home/user/documents/file.txt
   ```
   Kết quả: `file.txt`

2. Lấy tên tệp từ đường dẫn mà không có phần mở rộng:
   ```bash
   basename /home/user/documents/file.txt .txt
   ```
   Kết quả: `file`

3. Sử dụng tùy chọn `-a` để lấy tên tệp từ nhiều đường dẫn:
   ```bash
   basename -a /home/user/documents/file1.txt /home/user/documents/file2.txt
   ```
   Kết quả:
   ```
   file1.txt
   file2.txt
   ```

4. Xóa phần mở rộng từ nhiều tệp:
   ```bash
   basename -a /home/user/documents/file1.txt /home/user/documents/file2.log .txt .log
   ```
   Kết quả:
   ```
   file1
   file2
   ```

## Mẹo
- Sử dụng `basename` trong các kịch bản để dễ dàng xử lý tên tệp.
- Kết hợp với các lệnh khác như `find` để lấy tên tệp từ kết quả tìm kiếm.
- Hãy chắc chắn rằng bạn chỉ định đúng phần mở rộng nếu bạn muốn loại bỏ nó, để tránh mất tên tệp quan trọng.