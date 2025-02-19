# [Hệ điều hành] C Shell (csh) printf Cách sử dụng: In định dạng văn bản

## Overview
Lệnh `printf` trong C Shell (csh) được sử dụng để in ra văn bản với định dạng cụ thể. Nó cho phép người dùng kiểm soát cách thức hiển thị dữ liệu, bao gồm cả kiểu dữ liệu và cách trình bày.

## Usage
Cú pháp cơ bản của lệnh `printf` như sau:

```csh
printf [options] [arguments]
```

## Common Options
- `-v`: Gán giá trị cho biến.
- `-f`: Chỉ định định dạng cho đầu ra.
- `-n`: Không in ra ký tự xuống dòng ở cuối.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `printf`:

1. In một chuỗi đơn giản:
   ```csh
   printf "Hello, World!\n"
   ```

2. In số với định dạng:
   ```csh
   printf "Số nguyên: %d\n" 42
   ```

3. In số thực với 2 chữ số thập phân:
   ```csh
   printf "Số thực: %.2f\n" 3.14159
   ```

4. Gán giá trị cho biến và in ra:
   ```csh
   set var = "C Shell"
   printf "Chào mừng đến với %s!\n" $var
   ```

## Tips
- Sử dụng định dạng rõ ràng để đảm bảo đầu ra dễ đọc.
- Kiểm tra kỹ các tham số đầu vào để tránh lỗi khi in ra.
- Thực hành với các định dạng khác nhau để làm quen với cách hoạt động của `printf`.