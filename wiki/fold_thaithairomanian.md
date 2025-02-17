# [Linux] Bash fold sử dụng: Cắt dòng văn bản

## Overview
Lệnh `fold` trong Bash được sử dụng để cắt các dòng văn bản dài thành các dòng ngắn hơn với độ dài xác định. Điều này rất hữu ích khi bạn muốn định dạng văn bản cho các thiết bị có chiều rộng màn hình hạn chế hoặc khi bạn cần xử lý văn bản trong các tập tin.

## Usage
Cú pháp cơ bản của lệnh `fold` như sau:
```bash
fold [options] [arguments]
```

## Common Options
- `-w, --width=N`: Đặt chiều rộng tối đa cho mỗi dòng (mặc định là 80 ký tự).
- `-s, --spaces`: Cắt dòng tại khoảng trắng gần nhất trước khi đạt đến chiều rộng tối đa.
- `-b, --bytes`: Đếm chiều rộng bằng byte thay vì ký tự.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `fold`:

1. Cắt một tệp văn bản với chiều rộng mặc định:
   ```bash
   fold input.txt
   ```

2. Cắt một tệp văn bản với chiều rộng 50 ký tự:
   ```bash
   fold -w 50 input.txt
   ```

3. Cắt một tệp văn bản và cắt tại khoảng trắng gần nhất:
   ```bash
   fold -s -w 50 input.txt
   ```

4. Cắt một chuỗi văn bản trực tiếp từ dòng lệnh:
   ```bash
   echo "This is a long line of text that needs to be folded." | fold -w 30
   ```

## Tips
- Sử dụng tùy chọn `-s` để đảm bảo rằng các từ không bị cắt giữa chừng, giúp văn bản dễ đọc hơn.
- Kiểm tra chiều rộng của thiết bị đầu ra của bạn trước khi chọn chiều rộng cho lệnh `fold` để đảm bảo rằng văn bản được hiển thị đúng cách.
- Kết hợp `fold` với các lệnh khác như `cat` hoặc `grep` để xử lý văn bản một cách hiệu quả hơn.