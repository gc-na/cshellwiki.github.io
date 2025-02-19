# [Hệ điều hành] C Shell (csh) uniq Cách sử dụng: Lọc các dòng trùng lặp trong tệp

## Overview
Lệnh `uniq` trong C Shell (csh) được sử dụng để loại bỏ các dòng trùng lặp liên tiếp trong một tệp hoặc đầu vào từ dòng lệnh. Điều này rất hữu ích khi bạn muốn làm sạch dữ liệu hoặc chỉ cần giữ lại các dòng duy nhất.

## Usage
Cú pháp cơ bản của lệnh `uniq` như sau:
```
uniq [options] [arguments]
```

## Common Options
- `-c`: Đếm số lần xuất hiện của mỗi dòng.
- `-d`: Chỉ hiển thị các dòng trùng lặp.
- `-u`: Chỉ hiển thị các dòng duy nhất (không trùng lặp).
- `-i`: Bỏ qua sự khác biệt về chữ hoa và chữ thường.

## Common Examples
- **Loại bỏ các dòng trùng lặp trong tệp:**
```bash
uniq input.txt output.txt
```

- **Đếm số lần xuất hiện của mỗi dòng:**
```bash
uniq -c input.txt
```

- **Chỉ hiển thị các dòng trùng lặp:**
```bash
uniq -d input.txt
```

- **Chỉ hiển thị các dòng duy nhất:**
```bash
uniq -u input.txt
```

- **Bỏ qua sự khác biệt về chữ hoa và chữ thường:**
```bash
uniq -i input.txt output.txt
```

## Tips
- Đảm bảo rằng tệp đầu vào đã được sắp xếp trước khi sử dụng `uniq`, vì lệnh này chỉ loại bỏ các dòng trùng lặp liên tiếp.
- Sử dụng `sort` kết hợp với `uniq` để xử lý các dòng trùng lặp không liên tiếp:
```bash
sort input.txt | uniq
```
- Kiểm tra kết quả bằng cách sử dụng `cat` để xem nội dung của tệp đầu ra sau khi thực hiện lệnh `uniq`.