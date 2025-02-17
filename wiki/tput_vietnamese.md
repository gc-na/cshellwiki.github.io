# [Linux] Bash tput cách sử dụng: Điều chỉnh định dạng đầu ra trong terminal

## Tổng quan
Lệnh `tput` được sử dụng để điều chỉnh định dạng đầu ra trong terminal, cho phép người dùng thay đổi màu sắc, định dạng văn bản và các thuộc tính khác của giao diện dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tput` như sau:
```
tput [options] [arguments]
```

## Các tùy chọn phổ biến
- `setaf [n]`: Thiết lập màu chữ (foreground) với `n` là số màu.
- `setab [n]`: Thiết lập màu nền (background) với `n` là số màu.
- `bold`: Bật chế độ chữ đậm.
- `smso`: Bật chế độ in nghiêng (standout mode).
- `rmso`: Tắt chế độ in nghiêng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `tput`:

1. **Thay đổi màu chữ thành đỏ**:
   ```bash
   tput setaf 1
   echo "Đây là văn bản màu đỏ"
   tput sgr0  # Đặt lại định dạng
   ```

2. **Thay đổi màu nền thành xanh lá cây**:
   ```bash
   tput setab 2
   echo "Đây là văn bản với nền màu xanh lá cây"
   tput sgr0  # Đặt lại định dạng
   ```

3. **Bật chế độ chữ đậm**:
   ```bash
   tput bold
   echo "Đây là văn bản đậm"
   tput sgr0  # Đặt lại định dạng
   ```

4. **Sử dụng chế độ in nghiêng**:
   ```bash
   tput smso
   echo "Đây là văn bản in nghiêng"
   tput rmso  # Tắt chế độ in nghiêng
   ```

## Mẹo
- Luôn sử dụng `tput sgr0` sau khi thay đổi định dạng để đặt lại các thuộc tính về mặc định.
- Kiểm tra danh sách màu sắc và mã số của chúng trên hệ thống của bạn để sử dụng chính xác với lệnh `tput`.
- Kết hợp `tput` với các lệnh khác trong shell script để tạo ra các giao diện người dùng trực quan hơn.