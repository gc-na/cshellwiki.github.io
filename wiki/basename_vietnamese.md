# [Hệ điều hành] C Shell (csh) basename Cách sử dụng: Lấy tên tệp từ đường dẫn

## Overview
Lệnh `basename` trong C Shell được sử dụng để trích xuất tên tệp từ một đường dẫn đầy đủ. Nó giúp người dùng dễ dàng lấy tên tệp mà không cần phải biết đến phần đường dẫn.

## Usage
Cú pháp cơ bản của lệnh `basename` như sau:
```csh
basename [options] [arguments]
```

## Common Options
- `-a`: Trả về tất cả các tên tệp từ danh sách đường dẫn.
- `-s`: Loại bỏ phần mở rộng tệp được chỉ định.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `basename`:

1. Lấy tên tệp từ đường dẫn:
   ```csh
   basename /home/user/document.txt
   ```
   Kết quả: `document.txt`

2. Lấy tên tệp từ nhiều đường dẫn:
   ```csh
   basename -a /home/user/file1.txt /home/user/file2.txt
   ```
   Kết quả: 
   ```
   file1.txt
   file2.txt
   ```

3. Loại bỏ phần mở rộng tệp:
   ```csh
   basename -s .txt /home/user/report.txt
   ```
   Kết quả: `report`

## Tips
- Sử dụng `basename` khi bạn chỉ cần tên tệp mà không cần biết đến đường dẫn.
- Kết hợp với các lệnh khác như `find` để xử lý nhiều tệp cùng lúc.
- Hãy chú ý đến phần mở rộng tệp nếu bạn sử dụng tùy chọn `-s` để đảm bảo loại bỏ đúng phần mở rộng.