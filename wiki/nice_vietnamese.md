# [Hệ điều hành] C Shell (csh) nice: Điều chỉnh ưu tiên của tiến trình

## Overview
Lệnh `nice` trong C Shell (csh) được sử dụng để điều chỉnh mức độ ưu tiên của một tiến trình khi nó được thực thi. Bằng cách thay đổi mức độ ưu tiên, bạn có thể kiểm soát cách mà hệ thống phân bổ tài nguyên cho các tiến trình đang chạy.

## Usage
Cú pháp cơ bản của lệnh `nice` như sau:
```
nice [options] [arguments]
```

## Common Options
- `-n <value>`: Chỉ định giá trị ưu tiên mới cho tiến trình. Giá trị này có thể từ -20 (ưu tiên cao nhất) đến 19 (ưu tiên thấp nhất).
- `-h`: Hiển thị thông tin trợ giúp về lệnh `nice`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `nice`:

1. **Chạy một tiến trình với ưu tiên thấp hơn**:
   ```csh
   nice -n 10 ./my_script.sh
   ```

2. **Chạy một tiến trình với ưu tiên cao hơn**:
   ```csh
   nice -n -5 ./my_heavy_process
   ```

3. **Kiểm tra ưu tiên của một tiến trình đang chạy**:
   ```csh
   ps -o pid,ni,cmd
   ```

4. **Chạy một lệnh `make` với ưu tiên thấp**:
   ```csh
   nice -n 15 make
   ```

## Tips
- Sử dụng `nice` để giảm tải cho hệ thống khi chạy các tiến trình nặng, giúp hệ thống hoạt động mượt mà hơn.
- Kiểm tra ưu tiên của các tiến trình đang chạy bằng lệnh `ps` để có cái nhìn tổng quan về tài nguyên hệ thống.
- Hãy cẩn thận khi tăng ưu tiên của một tiến trình, vì điều này có thể làm giảm hiệu suất của các tiến trình khác.