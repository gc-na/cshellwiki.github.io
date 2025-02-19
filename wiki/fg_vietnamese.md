# [Hệ điều hành] C Shell (csh) fg Cách sử dụng: Kích hoạt tiến trình nền

## Tổng quan
Lệnh `fg` trong C Shell (csh) được sử dụng để đưa một tiến trình đang chạy ở chế độ nền trở lại chế độ foreground (trước). Điều này cho phép người dùng tương tác với tiến trình đó trực tiếp từ dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `fg` như sau:
```
fg [options] [arguments]
```

## Các tùy chọn phổ biến
- `job_spec`: Chỉ định tiến trình cụ thể mà bạn muốn đưa về foreground. Bạn có thể sử dụng số thứ tự của tiến trình hoặc tên của nó.
- `-l`: Hiển thị danh sách các tiến trình đang chạy.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `fg`:

1. Đưa tiến trình gần nhất về foreground:
   ```csh
   fg
   ```

2. Đưa một tiến trình cụ thể (ví dụ tiến trình số 1) về foreground:
   ```csh
   fg %1
   ```

3. Nếu bạn có nhiều tiến trình đang chạy, bạn có thể xem danh sách các tiến trình với lệnh `jobs` trước khi sử dụng `fg`:
   ```csh
   jobs
   fg %2
   ```

## Mẹo
- Sử dụng lệnh `jobs` để kiểm tra các tiến trình đang chạy trước khi sử dụng `fg`, giúp bạn biết chính xác tiến trình nào cần được đưa về foreground.
- Nếu bạn muốn dừng một tiến trình đang chạy ở foreground, bạn có thể sử dụng tổ hợp phím `Ctrl + Z` để tạm dừng nó và sau đó sử dụng `fg` để tiếp tục.
- Hãy nhớ rằng chỉ có thể đưa các tiến trình đã được khởi động từ phiên làm việc hiện tại về foreground.