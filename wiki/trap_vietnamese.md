# [Hệ điều hành] C Shell (csh) trap Cách sử dụng: Quản lý tín hiệu trong shell

## Tổng quan
Lệnh `trap` trong C Shell (csh) được sử dụng để thiết lập các hành động cụ thể khi nhận được tín hiệu nhất định. Điều này rất hữu ích để xử lý các tình huống như dừng hoặc thoát khỏi một script một cách an toàn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `trap` như sau:

```
trap [options] [arguments]
```

## Các tùy chọn phổ biến
- `SIGINT`: Tín hiệu ngắt (Ctrl+C).
- `SIGTERM`: Tín hiệu yêu cầu dừng chương trình.
- `EXIT`: Hành động sẽ được thực hiện khi script kết thúc.
- `DEBUG`: Hành động sẽ được thực hiện trước mỗi lệnh trong script.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `trap`:

1. **Bắt tín hiệu ngắt (Ctrl+C)**:
   ```csh
   trap 'echo "Script bị ngắt"; exit' SIGINT
   while true; do
       echo "Đang chạy..."
       sleep 1
   end
   ```

2. **Thực hiện hành động khi script kết thúc**:
   ```csh
   trap 'echo "Script đã kết thúc."' EXIT
   echo "Chạy một số lệnh..."
   ```

3. **Bắt tín hiệu dừng**:
   ```csh
   trap 'echo "Nhận tín hiệu dừng"; exit' SIGTERM
   while true; do
       echo "Chạy liên tục..."
       sleep 2
   end
   ```

## Mẹo
- Sử dụng `trap` để đảm bảo rằng các tài nguyên được giải phóng hoặc các hành động cần thiết được thực hiện khi script kết thúc.
- Đặt các lệnh `trap` ở đầu script để đảm bảo rằng chúng luôn được thiết lập trước khi bất kỳ lệnh nào khác được thực hiện.
- Kiểm tra các tín hiệu có thể được sử dụng với lệnh `trap` bằng cách tham khảo tài liệu hoặc sử dụng lệnh `kill -l` để xem danh sách các tín hiệu.