# [Linux] Bash fold cách sử dụng: Cắt dòng văn bản

## Overview
Lệnh `fold` trong Bash được sử dụng để cắt các dòng văn bản dài thành các dòng ngắn hơn, giúp dễ dàng đọc và hiển thị trên màn hình. Lệnh này rất hữu ích khi bạn muốn định dạng văn bản cho phù hợp với kích thước của cửa sổ terminal.

## Usage
Cú pháp cơ bản của lệnh `fold` như sau:
```
fold [options] [arguments]
```

## Common Options
- `-w, --width=N`: Chỉ định chiều rộng tối đa cho mỗi dòng. Mặc định là 80 ký tự.
- `-s, --spaces`: Cắt dòng tại khoảng trắng gần nhất trước khi vượt quá chiều rộng chỉ định.
- `-b, --bytes`: Đếm số ký tự theo byte thay vì theo ký tự.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `fold`:

1. Cắt một tệp văn bản với chiều rộng mặc định (80 ký tự):
   ```bash
   fold input.txt
   ```

2. Cắt một tệp văn bản với chiều rộng 50 ký tự:
   ```bash
   fold -w 50 input.txt
   ```

3. Cắt dòng tại khoảng trắng gần nhất với chiều rộng 30 ký tự:
   ```bash
   fold -w 30 -s input.txt
   ```

4. Cắt một chuỗi văn bản trực tiếp từ dòng lệnh:
   ```bash
   echo "Đây là một ví dụ về việc sử dụng lệnh fold trong Bash." | fold -w 40
   ```

## Tips
- Sử dụng tùy chọn `-s` để đảm bảo rằng các từ không bị cắt giữa chừng, giúp văn bản dễ đọc hơn.
- Kết hợp lệnh `fold` với các lệnh khác như `cat` hoặc `echo` để xử lý văn bản một cách linh hoạt.
- Kiểm tra chiều rộng của terminal của bạn để điều chỉnh chiều rộng cắt cho phù hợp, tránh việc cắt dòng không cần thiết.