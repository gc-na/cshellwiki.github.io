# [Hệ điều hành] C Shell (csh) expr Cách sử dụng: Tính toán và so sánh biểu thức

## Overview
Lệnh `expr` trong C Shell (csh) được sử dụng để thực hiện các phép toán số học, so sánh và xử lý chuỗi. Nó cho phép người dùng thực hiện các phép toán đơn giản trong dòng lệnh.

## Usage
Cú pháp cơ bản của lệnh `expr` như sau:
```
expr [options] [arguments]
```

## Common Options
- `+` : Phép cộng.
- `-` : Phép trừ.
- `*` : Phép nhân.
- `/` : Phép chia.
- `%` : Phép chia lấy dư.
- `=` : So sánh bằng.
- `!=` : So sánh khác.
- `<` : So sánh nhỏ hơn.
- `>` : So sánh lớn hơn.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `expr`:

1. **Phép cộng hai số:**
   ```csh
   expr 5 + 3
   ```
   Kết quả sẽ là `8`.

2. **Phép trừ hai số:**
   ```csh
   expr 10 - 4
   ```
   Kết quả sẽ là `6`.

3. **Phép nhân hai số:**
   ```csh
   expr 7 \* 3
   ```
   Kết quả sẽ là `21`.

4. **Phép chia hai số:**
   ```csh
   expr 20 / 4
   ```
   Kết quả sẽ là `5`.

5. **So sánh hai số:**
   ```csh
   expr 5 = 5
   ```
   Kết quả sẽ là `1` (đúng).

6. **So sánh chuỗi:**
   ```csh
   expr "hello" = "hello"
   ```
   Kết quả sẽ là `1` (đúng).

## Tips
- Khi sử dụng phép nhân (`*`), hãy nhớ thêm dấu gạch chéo ngược (`\`) trước ký tự để tránh nhầm lẫn với ký tự wildcard.
- Sử dụng dấu ngoặc đơn để nhóm các phép toán phức tạp nhằm đảm bảo thứ tự thực hiện chính xác.
- Lệnh `expr` chỉ hỗ trợ số nguyên, vì vậy hãy cẩn thận khi làm việc với số thực.