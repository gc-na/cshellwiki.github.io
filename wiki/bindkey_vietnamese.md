# [Linux] Bash bindkey cách sử dụng: Gán phím tắt cho các lệnh

## Tổng quan
Lệnh `bindkey` trong Bash được sử dụng để gán các phím tắt cho các lệnh hoặc hành động trong môi trường dòng lệnh. Điều này giúp người dùng thao tác nhanh hơn và hiệu quả hơn khi sử dụng terminal.

## Cách sử dụng
Cú pháp cơ bản của lệnh `bindkey` như sau:

```bash
bindkey [options] [arguments]
```

## Các tùy chọn phổ biến
- `-e`: Sử dụng chế độ vi (Emacs) cho các phím tắt.
- `-v`: Sử dụng chế độ vim cho các phím tắt.
- `-p`: Hiển thị danh sách các phím tắt hiện tại.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `bindkey`:

1. **Gán phím tắt cho lệnh clear**:
   ```bash
   bindkey -s '^K' 'clear\n'
   ```
   Khi bạn nhấn `Ctrl + K`, terminal sẽ xóa màn hình.

2. **Chuyển sang chế độ vi**:
   ```bash
   bindkey -v
   ```
   Điều này sẽ chuyển chế độ phím tắt sang chế độ vim.

3. **Hiển thị các phím tắt hiện tại**:
   ```bash
   bindkey -p
   ```
   Lệnh này sẽ hiển thị danh sách các phím tắt đã được gán.

## Mẹo
- Hãy thử gán các phím tắt cho các lệnh mà bạn sử dụng thường xuyên để tiết kiệm thời gian.
- Để dễ dàng nhớ các phím tắt, hãy ghi chú lại hoặc tạo một tệp cấu hình cho các gán phím của bạn.
- Kiểm tra các phím tắt hiện tại thường xuyên để tránh xung đột giữa các lệnh.