# [Linux] Bash mv sử dụng: Di chuyển hoặc đổi tên tệp

## Overview
Lệnh `mv` trong Bash được sử dụng để di chuyển hoặc đổi tên các tệp và thư mục. Khi bạn muốn thay đổi vị trí của một tệp hoặc thư mục, hoặc chỉ đơn giản là muốn đổi tên chúng, lệnh này sẽ giúp bạn thực hiện điều đó một cách dễ dàng.

## Usage
Cú pháp cơ bản của lệnh `mv` như sau:
```bash
mv [options] [arguments]
```

## Common Options
- `-i`: Yêu cầu xác nhận trước khi ghi đè lên tệp đích.
- `-u`: Chỉ di chuyển tệp nếu tệp nguồn mới hơn tệp đích hoặc nếu tệp đích không tồn tại.
- `-v`: Hiển thị thông tin chi tiết về các tệp đang được di chuyển.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mv`:

1. **Di chuyển một tệp đến thư mục khác:**
   ```bash
   mv file.txt /path/to/destination/
   ```

2. **Đổi tên một tệp:**
   ```bash
   mv oldname.txt newname.txt
   ```

3. **Di chuyển nhiều tệp đến một thư mục:**
   ```bash
   mv file1.txt file2.txt /path/to/destination/
   ```

4. **Di chuyển và yêu cầu xác nhận trước khi ghi đè:**
   ```bash
   mv -i file.txt /path/to/destination/
   ```

## Tips
- Sử dụng tùy chọn `-i` để tránh ghi đè lên các tệp quan trọng một cách không mong muốn.
- Kiểm tra kỹ đường dẫn đích trước khi thực hiện lệnh để đảm bảo bạn không di chuyển tệp đến vị trí sai.
- Khi đổi tên tệp, hãy chắc chắn rằng tên mới không trùng với tên của tệp khác trong cùng thư mục.