# [Linux] Bash wc sử dụng: Đếm số dòng, từ và ký tự trong tệp

## Overview
Lệnh `wc` (word count) trong Bash được sử dụng để đếm số dòng, từ và ký tự trong một hoặc nhiều tệp. Đây là một công cụ hữu ích để phân tích nội dung của tệp văn bản.

## Usage
Cú pháp cơ bản của lệnh `wc` như sau:
```bash
wc [options] [arguments]
```

## Common Options
- `-l`: Đếm số dòng.
- `-w`: Đếm số từ.
- `-c`: Đếm số ký tự.
- `-m`: Đếm số ký tự (bao gồm cả ký tự Unicode).
- `-L`: Hiển thị độ dài của dòng dài nhất.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `wc`:

1. Đếm số dòng trong một tệp:
   ```bash
   wc -l filename.txt
   ```

2. Đếm số từ trong một tệp:
   ```bash
   wc -w filename.txt
   ```

3. Đếm số ký tự trong một tệp:
   ```bash
   wc -c filename.txt
   ```

4. Đếm số dòng, từ và ký tự cùng một lúc:
   ```bash
   wc filename.txt
   ```

5. Đếm số ký tự trong một tệp với ký tự Unicode:
   ```bash
   wc -m filename.txt
   ```

## Tips
- Bạn có thể sử dụng `wc` kết hợp với các lệnh khác bằng cách sử dụng ống (pipe). Ví dụ, để đếm số dòng của kết quả từ lệnh `grep`, bạn có thể làm như sau:
  ```bash
  grep "pattern" filename.txt | wc -l
  ```
- Nếu bạn cần đếm nhiều tệp cùng một lúc, chỉ cần liệt kê các tệp sau lệnh `wc`:
  ```bash
  wc file1.txt file2.txt
  ```
- Hãy nhớ rằng `wc` có thể hoạt động với đầu vào từ bàn phím nếu không có tệp nào được chỉ định. Bạn có thể kết thúc đầu vào bằng cách nhấn `Ctrl+D`.