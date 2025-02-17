# [Bash] Bash true sử dụng: Xác nhận thành công

## Overview
Lệnh `true` trong Bash là một lệnh đơn giản được sử dụng để trả về giá trị thành công (0). Nó thường được sử dụng trong các kịch bản và lệnh để xác nhận rằng một điều gì đó đã thành công mà không thực hiện bất kỳ hành động nào.

## Usage
Cú pháp cơ bản của lệnh `true` như sau:
```bash
true [options] [arguments]
```

## Common Options
Lệnh `true` không có tùy chọn nào cụ thể. Nó chỉ đơn giản là một lệnh mà không cần tham số.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `true`:

1. **Kiểm tra điều kiện trong một kịch bản:**
   ```bash
   if true; then
       echo "Điều kiện đúng!"
   fi
   ```

2. **Sử dụng trong vòng lặp:**
   ```bash
   while true; do
       echo "Vòng lặp đang chạy..."
       sleep 1
   done
   ```

3. **Kết hợp với lệnh khác:**
   ```bash
   command || true
   ```

## Tips
- Lệnh `true` có thể được sử dụng để tạo ra các vòng lặp vô hạn trong các kịch bản, nhưng hãy cẩn thận để không làm treo hệ thống.
- Sử dụng `true` trong các kịch bản để đảm bảo rằng các lệnh tiếp theo sẽ được thực hiện ngay cả khi lệnh trước đó thất bại.