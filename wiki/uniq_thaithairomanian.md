# [Bash] Bash uniq sử dụng: Lọc các dòng trùng lặp trong tệp

## Overview
Lệnh `uniq` trong Bash được sử dụng để loại bỏ các dòng trùng lặp liên tiếp trong một tệp hoặc đầu ra của một lệnh khác. Điều này rất hữu ích khi bạn muốn làm sạch dữ liệu và chỉ giữ lại các dòng duy nhất.

## Usage
Cú pháp cơ bản của lệnh `uniq` như sau:
```
uniq [options] [arguments]
```

## Common Options
- `-c`: Đếm số lần xuất hiện của mỗi dòng.
- `-d`: Chỉ hiển thị các dòng trùng lặp.
- `-u`: Chỉ hiển thị các dòng duy nhất.
- `-i`: Bỏ qua sự khác biệt giữa chữ hoa và chữ thường.

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

- **Bỏ qua sự khác biệt giữa chữ hoa và chữ thường:**
  ```bash
  uniq -i input.txt
  ```

## Tips
- Để `uniq` hoạt động chính xác, bạn nên sắp xếp tệp đầu vào trước khi sử dụng lệnh này, vì `uniq` chỉ loại bỏ các dòng trùng lặp liên tiếp.
- Kết hợp `uniq` với lệnh `sort` để xử lý dữ liệu hiệu quả hơn:
  ```bash
  sort input.txt | uniq
  ```
- Sử dụng `-c` để có cái nhìn tổng quan về tần suất xuất hiện của các dòng, điều này có thể giúp bạn phân tích dữ liệu tốt hơn.