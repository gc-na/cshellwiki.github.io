# [Linux] Bash wc Cách sử dụng: Đếm số dòng, từ và ký tự trong tệp

## Overview
Lệnh `wc` (word count) trong Bash được sử dụng để đếm số dòng, số từ và số ký tự trong một hoặc nhiều tệp. Đây là một công cụ hữu ích cho việc phân tích nội dung tệp và thu thập thông tin cơ bản về chúng.

## Usage
Cú pháp cơ bản của lệnh `wc` như sau:
```
wc [options] [arguments]
```

## Common Options
- `-l`: Đếm số dòng trong tệp.
- `-w`: Đếm số từ trong tệp.
- `-c`: Đếm số ký tự trong tệp.
- `-m`: Đếm số ký tự (bao gồm cả ký tự Unicode).
- `-L`: Hiển thị độ dài của dòng dài nhất trong tệp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `wc`:

1. Đếm số dòng trong một tệp:
   ```bash
   wc -l ten_tap.txt
   ```

2. Đếm số từ trong một tệp:
   ```bash
   wc -w ten_tap.txt
   ```

3. Đếm số ký tự trong một tệp:
   ```bash
   wc -c ten_tap.txt
   ```

4. Đếm số dòng, số từ và số ký tự trong một tệp cùng một lúc:
   ```bash
   wc ten_tap.txt
   ```

5. Đếm số ký tự trong nhiều tệp:
   ```bash
   wc -c tap1.txt tap2.txt
   ```

## Tips
- Bạn có thể kết hợp nhiều tùy chọn trong một lệnh. Ví dụ, để đếm số dòng và số từ, bạn có thể sử dụng:
  ```bash
  wc -l -w ten_tap.txt
  ```
- Sử dụng `wc` cùng với các lệnh khác bằng cách sử dụng ống (pipe). Ví dụ, để đếm số dòng trong kết quả của lệnh `grep`:
  ```bash
  grep "chuỗi_cần_tìm" ten_tap.txt | wc -l
  ```
- Để dễ dàng đọc kết quả, bạn có thể sử dụng `-h` để hiển thị kết quả với định dạng dễ hiểu hơn.