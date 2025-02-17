# [Linux] Bash diff sử dụng: So sánh sự khác biệt giữa các tệp

## Overview
Lệnh `diff` trong Bash được sử dụng để so sánh nội dung của hai tệp hoặc thư mục. Nó hiển thị sự khác biệt giữa chúng, giúp người dùng nhận biết các thay đổi đã được thực hiện.

## Usage
Cú pháp cơ bản của lệnh `diff` như sau:
```bash
diff [options] [file1] [file2]
```

## Common Options
- `-u`: Hiển thị sự khác biệt theo định dạng thống nhất, dễ đọc hơn.
- `-i`: Bỏ qua sự khác biệt về chữ hoa và chữ thường.
- `-w`: Bỏ qua sự khác biệt về khoảng trắng.
- `-r`: So sánh các thư mục một cách đệ quy.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `diff`:

1. So sánh hai tệp:
   ```bash
   diff file1.txt file2.txt
   ```

2. So sánh hai tệp với định dạng thống nhất:
   ```bash
   diff -u file1.txt file2.txt
   ```

3. So sánh hai thư mục:
   ```bash
   diff -r dir1/ dir2/
   ```

4. So sánh hai tệp mà không phân biệt chữ hoa và chữ thường:
   ```bash
   diff -i file1.txt file2.txt
   ```

## Tips
- Sử dụng tùy chọn `-u` để có cái nhìn tổng quan hơn về sự khác biệt.
- Khi so sánh thư mục, hãy sử dụng tùy chọn `-r` để đảm bảo tất cả các tệp con đều được kiểm tra.
- Nếu bạn chỉ quan tâm đến sự khác biệt về nội dung mà không phải khoảng trắng, hãy sử dụng tùy chọn `-w`.