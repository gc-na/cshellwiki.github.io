# [Linux] Bash rm Cách sử dụng: Xóa tệp và thư mục

## Tổng quan
Lệnh `rm` trong Bash được sử dụng để xóa các tệp và thư mục. Đây là một công cụ mạnh mẽ, nhưng cần được sử dụng cẩn thận vì các tệp bị xóa sẽ không thể khôi phục lại dễ dàng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `rm` như sau:

```bash
rm [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-f`: Bỏ qua cảnh báo và xóa tệp mà không yêu cầu xác nhận.
- `-i`: Yêu cầu xác nhận trước khi xóa từng tệp.
- `-r`: Xóa thư mục và tất cả các tệp bên trong nó.
- `-v`: Hiển thị thông tin chi tiết về các tệp đang được xóa.

## Ví dụ phổ biến
- Xóa một tệp đơn giản:

```bash
rm ten_tap.txt
```

- Xóa nhiều tệp cùng lúc:

```bash
rm tap1.txt tap2.txt tap3.txt
```

- Xóa một thư mục và tất cả các tệp bên trong:

```bash
rm -r thu_muc/
```

- Xóa tệp mà không yêu cầu xác nhận:

```bash
rm -f ten_tap.txt
```

- Yêu cầu xác nhận trước khi xóa:

```bash
rm -i ten_tap.txt
```

## Mẹo
- Luôn kiểm tra lại tên tệp hoặc thư mục trước khi sử dụng lệnh `rm`, đặc biệt là với tùy chọn `-f` hoặc `-r`.
- Sử dụng tùy chọn `-i` để tránh xóa nhầm tệp quan trọng.
- Cân nhắc sử dụng lệnh `mv` để di chuyển tệp vào một thư mục tạm thời trước khi xóa, để có thể khôi phục nếu cần.