# [Linux] Bash uniq Cách sử dụng: Lọc các dòng trùng lặp trong tệp

## Overview
Lệnh `uniq` trong Bash được sử dụng để loại bỏ các dòng trùng lặp liên tiếp trong một tệp hoặc đầu vào từ dòng lệnh. Điều này rất hữu ích khi bạn muốn làm sạch dữ liệu hoặc chỉ cần giữ lại các dòng duy nhất.

## Usage
Cú pháp cơ bản của lệnh `uniq` như sau:
```bash
uniq [options] [arguments]
```

## Common Options
- `-c`: Đếm số lần xuất hiện của mỗi dòng và hiển thị số đó trước dòng.
- `-d`: Chỉ hiển thị các dòng trùng lặp.
- `-u`: Chỉ hiển thị các dòng duy nhất (không trùng lặp).
- `-i`: Bỏ qua sự khác biệt giữa chữ hoa và chữ thường khi so sánh.
- `-w N`: So sánh chỉ N ký tự đầu tiên của mỗi dòng.

## Common Examples
- **Loại bỏ các dòng trùng lặp trong một tệp:**
```bash
uniq input.txt output.txt
```
Lệnh này sẽ đọc từ `input.txt`, loại bỏ các dòng trùng lặp và lưu kết quả vào `output.txt`.

- **Đếm số lần xuất hiện của mỗi dòng:**
```bash
uniq -c input.txt
```
Lệnh này sẽ hiển thị số lần mỗi dòng xuất hiện trong `input.txt`.

- **Chỉ hiển thị các dòng trùng lặp:**
```bash
uniq -d input.txt
```
Lệnh này sẽ chỉ hiển thị các dòng trùng lặp trong `input.txt`.

- **Bỏ qua sự khác biệt giữa chữ hoa và chữ thường:**
```bash
uniq -i input.txt
```
Lệnh này sẽ loại bỏ các dòng trùng lặp mà không phân biệt chữ hoa và chữ thường.

## Tips
- Đảm bảo rằng tệp đầu vào đã được sắp xếp trước khi sử dụng `uniq`, vì lệnh này chỉ loại bỏ các dòng trùng lặp liên tiếp.
- Sử dụng `sort` trước `uniq` để xử lý các dòng trùng lặp không liên tiếp:
```bash
sort input.txt | uniq
```
- Kiểm tra kết quả bằng cách sử dụng `cat` hoặc `less` để xem nội dung của tệp đầu ra.