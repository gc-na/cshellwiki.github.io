# [Linux] Bash true cách sử dụng: Trả về giá trị đúng

## Overview
Lệnh `true` trong Bash là một lệnh đơn giản, nó chỉ trả về giá trị đúng (0) mà không thực hiện bất kỳ hành động nào khác. Lệnh này thường được sử dụng trong các kịch bản để biểu thị thành công hoặc để tạo ra một lệnh không làm gì.

## Usage
Cú pháp cơ bản của lệnh `true` như sau:

```bash
true [options] [arguments]
```

## Common Options
Lệnh `true` không có tùy chọn nào đặc biệt. Nó chỉ đơn giản là lệnh `true` mà không cần tham số.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `true`:

1. **Kiểm tra lệnh thành công**:
   ```bash
   if true; then
       echo "Lệnh thành công!"
   fi
   ```

2. **Sử dụng trong vòng lặp**:
   ```bash
   while true; do
       echo "Đang chạy..."
       sleep 1
   done
   ```

3. **Kết hợp với lệnh khác**:
   ```bash
   command && true
   ```

## Tips
- Lệnh `true` rất hữu ích khi bạn cần một lệnh không làm gì nhưng vẫn cần một giá trị trả về thành công.
- Bạn có thể sử dụng `true` trong các kịch bản để tạo ra các điều kiện hoặc vòng lặp vô hạn khi cần thiết.
- Kết hợp `true` với các lệnh khác có thể giúp bạn kiểm soát luồng thực thi trong các kịch bản phức tạp hơn.