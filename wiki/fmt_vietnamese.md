# [Linux] Bash fmt Cách sử dụng: Định dạng văn bản

## Overview
Lệnh `fmt` trong Bash được sử dụng để định dạng văn bản, giúp điều chỉnh chiều rộng của các dòng trong một tệp tin văn bản. Nó rất hữu ích khi bạn muốn làm cho văn bản dễ đọc hơn bằng cách tự động chia nhỏ các dòng dài thành các dòng ngắn hơn.

## Usage
Cú pháp cơ bản của lệnh fmt như sau:
```
fmt [options] [arguments]
```

## Common Options
- `-w, --width=N`: Đặt chiều rộng tối đa cho các dòng (mặc định là 75 ký tự).
- `-s, --split-only`: Chỉ chia các dòng mà không thay đổi chiều dài của chúng.
- `-p, --prefix=STRING`: Thêm một chuỗi vào đầu mỗi dòng.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `fmt`:

1. Định dạng một tệp văn bản với chiều rộng mặc định:
   ```bash
   fmt input.txt
   ```

2. Định dạng một tệp văn bản với chiều rộng 50 ký tự:
   ```bash
   fmt -w 50 input.txt
   ```

3. Chỉ chia các dòng mà không thay đổi chiều dài:
   ```bash
   fmt -s input.txt
   ```

4. Thêm một chuỗi vào đầu mỗi dòng:
   ```bash
   fmt -p ">> " input.txt
   ```

## Tips
- Sử dụng lệnh `cat` kết hợp với `fmt` để xem kết quả ngay lập tức:
  ```bash
  cat input.txt | fmt
  ```
- Thử nghiệm với các tùy chọn khác nhau để tìm ra định dạng phù hợp nhất cho văn bản của bạn.
- Nếu bạn làm việc với các tệp văn bản lớn, hãy lưu ý rằng `fmt` có thể không giữ nguyên định dạng của các đoạn văn bản phức tạp.