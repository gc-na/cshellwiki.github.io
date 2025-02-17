# [Linux] Bash comm sử dụng: So sánh hai tệp tin

## Overview
Lệnh `comm` trong Bash được sử dụng để so sánh hai tệp tin đã được sắp xếp và hiển thị các dòng khác nhau và giống nhau giữa chúng. Lệnh này hữu ích trong việc phân tích sự khác biệt giữa hai tệp tin văn bản.

## Usage
Cú pháp cơ bản của lệnh `comm` như sau:
```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Không hiển thị các dòng chỉ có trong tệp tin đầu tiên.
- `-2`: Không hiển thị các dòng chỉ có trong tệp tin thứ hai.
- `-3`: Không hiển thị các dòng giống nhau giữa hai tệp tin.
- `-i`: Bỏ qua sự khác biệt về chữ hoa chữ thường khi so sánh.

## Common Examples
1. So sánh hai tệp tin và hiển thị tất cả các dòng:
   ```bash
   comm file1.txt file2.txt
   ```

2. Chỉ hiển thị các dòng chỉ có trong `file1.txt`:
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. Chỉ hiển thị các dòng giống nhau:
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. So sánh hai tệp tin mà không phân biệt chữ hoa chữ thường:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- Đảm bảo rằng cả hai tệp tin được sắp xếp trước khi sử dụng lệnh `comm`, nếu không kết quả có thể không chính xác.
- Sử dụng các tùy chọn kết hợp để tinh chỉnh kết quả so sánh theo nhu cầu của bạn.
- Lưu ý rằng `comm` chỉ hoạt động với các tệp tin văn bản, vì vậy hãy kiểm tra định dạng tệp trước khi sử dụng.