# [Linux] Bash mv Cách sử dụng: Di chuyển hoặc đổi tên tệp

## Overview
Lệnh `mv` trong Bash được sử dụng để di chuyển hoặc đổi tên các tệp và thư mục. Khi bạn sử dụng lệnh này, bạn có thể chuyển tệp từ vị trí này sang vị trí khác hoặc thay đổi tên của tệp mà không cần tạo bản sao.

## Usage
Cú pháp cơ bản của lệnh `mv` như sau:

```bash
mv [options] [arguments]
```

## Common Options
- `-i`: Yêu cầu xác nhận trước khi ghi đè lên tệp đích nếu nó đã tồn tại.
- `-u`: Chỉ di chuyển tệp nếu tệp nguồn mới hơn tệp đích hoặc nếu tệp đích không tồn tại.
- `-v`: Hiển thị thông tin chi tiết về các tệp đang được di chuyển.

## Common Examples
1. **Di chuyển tệp từ một thư mục này sang thư mục khác:**
   ```bash
   mv /path/to/source/file.txt /path/to/destination/
   ```

2. **Đổi tên tệp:**
   ```bash
   mv oldname.txt newname.txt
   ```

3. **Di chuyển và ghi đè tệp mà không cần xác nhận:**
   ```bash
   mv -f /path/to/source/file.txt /path/to/destination/
   ```

4. **Di chuyển tệp và hiển thị thông tin chi tiết:**
   ```bash
   mv -v /path/to/source/file.txt /path/to/destination/
   ```

## Tips
- Sử dụng tùy chọn `-i` để tránh ghi đè lên các tệp quan trọng một cách không mong muốn.
- Kiểm tra kỹ đường dẫn tệp trước khi thực hiện lệnh để đảm bảo không di chuyển nhầm tệp.
- Nếu bạn thường xuyên làm việc với nhiều tệp, hãy cân nhắc sử dụng `mv` trong các tập lệnh tự động để tiết kiệm thời gian.