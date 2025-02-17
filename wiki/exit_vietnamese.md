# [Linux] Bash exit: Thoát khỏi shell hoặc script

## Overview
Lệnh `exit` trong Bash được sử dụng để thoát khỏi một shell hoặc một script. Khi lệnh này được thực hiện, nó sẽ kết thúc phiên làm việc hiện tại và trả về một mã thoát cho hệ thống. Mã thoát này có thể được sử dụng để xác định trạng thái của quá trình trước đó.

## Usage
Cú pháp cơ bản của lệnh `exit` như sau:

```bash
exit [options] [n]
```

Trong đó `n` là mã thoát mà bạn muốn trả về. Nếu không chỉ định mã thoát, mặc định sẽ là mã thoát của lệnh cuối cùng được thực thi.

## Common Options
- `n`: Mã thoát mà bạn muốn trả về. Mã này thường là một số nguyên từ 0 đến 255, trong đó 0 thường biểu thị thành công và các số khác biểu thị lỗi.
- `-`: Nếu sử dụng dấu trừ, lệnh sẽ trả về mã thoát của lệnh cuối cùng.

## Common Examples

1. **Thoát khỏi shell với mã thoát 0 (thành công)**:
   ```bash
   exit 0
   ```

2. **Thoát khỏi shell với mã thoát 1 (lỗi)**:
   ```bash
   exit 1
   ```

3. **Thoát khỏi một script mà không chỉ định mã thoát**:
   ```bash
   #!/bin/bash
   echo "Kết thúc script"
   exit
   ```

4. **Sử dụng mã thoát của lệnh trước đó**:
   ```bash
   ls /khong_ton_tai
   exit $?
   ```

## Tips
- Luôn sử dụng mã thoát 0 để biểu thị thành công và các mã khác để biểu thị lỗi, điều này giúp dễ dàng theo dõi trạng thái của script.
- Khi viết script, hãy đảm bảo rằng bạn sử dụng `exit` ở những vị trí hợp lý để ngăn chặn việc thực hiện các lệnh không cần thiết sau khi đã xảy ra lỗi.
- Bạn có thể kiểm tra mã thoát của lệnh cuối cùng bằng cách sử dụng biến `$?` ngay sau khi lệnh đó được thực thi.