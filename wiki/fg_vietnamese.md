# [Linux] Bash fg Cách sử dụng: Chuyển đổi tiến trình nền sang nền trước

## Tổng quan
Lệnh `fg` trong Bash được sử dụng để đưa một tiến trình đang chạy ở chế độ nền (background) trở lại chế độ nền trước (foreground). Điều này cho phép người dùng tương tác với tiến trình đó, như nhập dữ liệu hoặc nhận đầu ra trực tiếp.

## Cách sử dụng
Cú pháp cơ bản của lệnh `fg` như sau:
```
fg [options] [job_spec]
```

## Tùy chọn phổ biến
- `job_spec`: Chỉ định tiến trình cụ thể mà bạn muốn đưa về chế độ nền trước. Bạn có thể sử dụng số thứ tự của tiến trình hoặc ký hiệu `%` theo sau là số hoặc tên của tiến trình.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `fg`:

1. Đưa tiến trình nền gần nhất về chế độ nền trước:
   ```bash
   fg
   ```

2. Đưa một tiến trình cụ thể về chế độ nền trước bằng số thứ tự:
   ```bash
   fg %1
   ```

3. Đưa một tiến trình cụ thể về chế độ nền trước bằng tên:
   ```bash
   fg %my_process
   ```

## Mẹo
- Sử dụng lệnh `jobs` để xem danh sách các tiến trình đang chạy ở chế độ nền và xác định số thứ tự hoặc tên của tiến trình bạn muốn đưa về chế độ nền trước.
- Nếu bạn muốn tạm dừng một tiến trình đang chạy ở chế độ nền trước, bạn có thể sử dụng tổ hợp phím `Ctrl + Z` để tạm dừng và sau đó sử dụng `fg` để tiếp tục.
- Hãy chắc chắn rằng bạn đã lưu bất kỳ dữ liệu nào cần thiết trước khi đưa một tiến trình về chế độ nền trước, vì một số tiến trình có thể yêu cầu tương tác ngay lập tức.