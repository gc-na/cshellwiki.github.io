# [Linux] Bash killall cách sử dụng: Kết thúc tất cả tiến trình theo tên

## Tổng quan
Lệnh `killall` trong Bash được sử dụng để kết thúc tất cả các tiến trình đang chạy có cùng tên. Điều này rất hữu ích khi bạn muốn dừng một ứng dụng hoặc dịch vụ mà không cần phải tìm kiếm ID tiến trình (PID) của nó.

## Cách sử dụng
Cú pháp cơ bản của lệnh `killall` như sau:
```bash
killall [tùy chọn] [tên_tiến_trình]
```

## Tùy chọn phổ biến
- `-u <tên_người_dùng>`: Chỉ kết thúc các tiến trình của người dùng cụ thể.
- `-9`: Gửi tín hiệu SIGKILL để buộc dừng tiến trình ngay lập tức.
- `-q`: Không hiển thị thông báo lỗi nếu không tìm thấy tiến trình.
- `-r`: Sử dụng biểu thức chính quy để tìm kiếm tên tiến trình.

## Ví dụ phổ biến
Dưới đây là một số ví dụ về cách sử dụng lệnh `killall`:

1. Kết thúc tất cả các tiến trình có tên `firefox`:
   ```bash
   killall firefox
   ```

2. Kết thúc tất cả các tiến trình `gedit` với tín hiệu SIGKILL:
   ```bash
   killall -9 gedit
   ```

3. Kết thúc tất cả các tiến trình của người dùng `john`:
   ```bash
   killall -u john
   ```

4. Kết thúc tất cả các tiến trình có tên bắt đầu bằng `python` sử dụng biểu thức chính quy:
   ```bash
   killall -r '^python'
   ```

## Mẹo
- Luôn kiểm tra tên tiến trình trước khi sử dụng `killall` để tránh kết thúc nhầm tiến trình quan trọng.
- Sử dụng tùy chọn `-q` để giảm thiểu thông báo lỗi khi không tìm thấy tiến trình.
- Khi cần dừng một tiến trình một cách an toàn, hãy thử sử dụng tín hiệu SIGTERM (mặc định) trước khi sử dụng SIGKILL.