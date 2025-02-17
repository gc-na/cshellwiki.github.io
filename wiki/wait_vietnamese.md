# [Linux] Bash wait cách sử dụng: Chờ đợi tiến trình hoàn thành

## Tổng quan
Lệnh `wait` trong Bash được sử dụng để chờ đợi một hoặc nhiều tiến trình con hoàn thành. Khi lệnh này được gọi, nó sẽ tạm dừng thực thi cho đến khi tiến trình được chỉ định kết thúc, giúp quản lý các tiến trình một cách hiệu quả.

## Cách sử dụng
Cú pháp cơ bản của lệnh `wait` như sau:
```
wait [options] [arguments]
```

## Các tùy chọn phổ biến
- `-n`: Chờ cho bất kỳ tiến trình con nào hoàn thành.
- `-p`: Chờ cho một tiến trình cụ thể với PID đã cho.
- `[PID]`: Chỉ định PID của tiến trình mà bạn muốn chờ.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `wait`:

1. Chờ cho một tiến trình cụ thể hoàn thành:
   ```bash
   sleep 5 &
   pid=$!
   echo "Chờ cho tiến trình $pid hoàn thành..."
   wait $pid
   echo "Tiến trình đã hoàn thành."
   ```

2. Chờ cho tất cả các tiến trình con hoàn thành:
   ```bash
   for i in {1..3}; do
       sleep $i &
   done
   echo "Chờ cho tất cả các tiến trình hoàn thành..."
   wait
   echo "Tất cả các tiến trình đã hoàn thành."
   ```

3. Sử dụng tùy chọn `-n` để chờ cho bất kỳ tiến trình nào hoàn thành:
   ```bash
   for i in {1..3}; do
       sleep $i &
   done
   echo "Chờ cho bất kỳ tiến trình nào hoàn thành..."
   wait -n
   echo "Một tiến trình đã hoàn thành."
   ```

## Mẹo
- Sử dụng `wait` để đảm bảo rằng các tiến trình con đã hoàn thành trước khi tiếp tục thực hiện các lệnh khác trong script.
- Kiểm tra giá trị trả về của lệnh `wait` để xác định trạng thái của tiến trình đã chờ.
- Kết hợp `wait` với các lệnh khác trong Bash để tạo ra các script phức tạp hơn và hiệu quả hơn.