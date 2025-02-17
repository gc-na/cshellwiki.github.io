# [Linux] Bash nohup cách sử dụng: Chạy lệnh mà không bị ngắt kết nối

## Tổng quan
Lệnh `nohup` (viết tắt của "no hang up") cho phép bạn chạy một lệnh trong nền mà không bị ngắt kết nối khi bạn đăng xuất khỏi phiên làm việc. Điều này rất hữu ích khi bạn muốn thực hiện các tác vụ dài mà không cần phải giữ phiên terminal mở.

## Cách sử dụng
Cú pháp cơ bản của lệnh `nohup` như sau:

```bash
nohup [options] [arguments]
```

## Các tùy chọn phổ biến
- `&`: Chạy lệnh trong nền.
- `-h`: Hiển thị thông tin trợ giúp về lệnh.
- `-v`: Hiển thị thông tin chi tiết về quá trình thực hiện.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `nohup`:

1. Chạy một script Python trong nền:
   ```bash
   nohup python my_script.py &
   ```

2. Chạy một lệnh `ping` liên tục và lưu kết quả vào file:
   ```bash
   nohup ping google.com > ping_output.txt &
   ```

3. Chạy một lệnh `sleep` kéo dài 1 giờ:
   ```bash
   nohup sleep 3600 &
   ```

## Mẹo
- Sử dụng `&` để đảm bảo lệnh chạy trong nền, giúp bạn có thể tiếp tục sử dụng terminal.
- Kiểm tra file `nohup.out` để xem kết quả đầu ra của lệnh nếu không chỉ định file đầu ra khác.
- Đảm bảo rằng bạn đã kiểm tra các quyền truy cập cần thiết cho các file hoặc thư mục mà lệnh sẽ thao tác.