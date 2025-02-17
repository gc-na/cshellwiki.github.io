# [Linux] Bash unrar cách sử dụng: Giải nén tệp RAR

## Tổng quan
Lệnh `unrar` được sử dụng để giải nén các tệp tin định dạng RAR. Đây là một công cụ hữu ích cho việc truy cập và quản lý nội dung của các tệp nén RAR trên hệ thống Linux.

## Cách sử dụng
Cú pháp cơ bản của lệnh `unrar` như sau:

```bash
unrar [options] [arguments]
```

## Các tùy chọn phổ biến
- `x`: Giải nén tệp vào thư mục hiện tại.
- `e`: Giải nén tệp mà không giữ lại cấu trúc thư mục.
- `l`: Liệt kê nội dung của tệp RAR mà không giải nén.
- `t`: Kiểm tra tính toàn vẹn của tệp RAR.
- `v`: Hiển thị thông tin chi tiết về tệp RAR.

## Ví dụ thường gặp
- Giải nén tệp RAR vào thư mục hiện tại:

```bash
unrar x tenfile.rar
```

- Giải nén tệp RAR vào một thư mục cụ thể:

```bash
unrar x tenfile.rar /duongdan/thu_muc/
```

- Liệt kê nội dung của tệp RAR:

```bash
unrar l tenfile.rar
```

- Kiểm tra tính toàn vẹn của tệp RAR:

```bash
unrar t tenfile.rar
```

## Mẹo
- Luôn kiểm tra tính toàn vẹn của tệp RAR trước khi giải nén để đảm bảo không có lỗi.
- Sử dụng tùy chọn `e` nếu bạn chỉ muốn giải nén các tệp mà không cần cấu trúc thư mục.
- Đảm bảo rằng bạn có quyền truy cập vào thư mục nơi bạn muốn giải nén tệp.