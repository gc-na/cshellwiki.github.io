# [Hệ điều hành Unix] C Shell (csh) wc Cách sử dụng: Đếm số dòng, từ và ký tự trong tệp

## Overview
Lệnh `wc` (word count) trong C Shell được sử dụng để đếm số dòng, số từ và số ký tự trong một hoặc nhiều tệp. Đây là một công cụ hữu ích để phân tích nội dung của tệp văn bản.

## Usage
Cú pháp cơ bản của lệnh `wc` như sau:
```
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

1. Đếm số dòng, từ và ký tự trong một tệp:
   ```csh
   wc filename.txt
   ```

2. Chỉ đếm số dòng trong một tệp:
   ```csh
   wc -l filename.txt
   ```

3. Chỉ đếm số từ trong một tệp:
   ```csh
   wc -w filename.txt
   ```

4. Đếm số ký tự trong một tệp:
   ```csh
   wc -c filename.txt
   ```

5. Đếm số dòng trong nhiều tệp:
   ```csh
   wc -l file1.txt file2.txt
   ```

## Tips
- Khi sử dụng `wc`, bạn có thể kết hợp nhiều tùy chọn cùng một lúc. Ví dụ, để đếm số dòng và số từ, bạn có thể sử dụng:
  ```csh
  wc -l -w filename.txt
  ```
- Để dễ dàng hơn trong việc phân tích nhiều tệp, bạn có thể sử dụng ký tự đại diện. Ví dụ:
  ```csh
  wc *.txt
  ```
- Lưu ý rằng kết quả của `wc` sẽ hiển thị số liệu cho từng tệp và tổng số liệu cho tất cả các tệp nếu bạn cung cấp nhiều tệp.