# [Linux] Bash 7z Cách sử dụng: Nén và giải nén tập tin

## Tổng quan
Lệnh `7z` là một công cụ mạnh mẽ để nén và giải nén các tập tin. Nó hỗ trợ nhiều định dạng nén khác nhau và cho phép người dùng quản lý các tập tin nén một cách hiệu quả.

## Cách sử dụng
Cú pháp cơ bản của lệnh `7z` như sau:
```
7z [options] [arguments]
```

## Các tùy chọn phổ biến
- `a`: Thêm tập tin vào một tập tin nén.
- `x`: Giải nén tập tin.
- `l`: Liệt kê nội dung của tập tin nén.
- `d`: Xóa tập tin từ tập tin nén.
- `t`: Kiểm tra tính toàn vẹn của tập tin nén.

## Ví dụ thường gặp
- Nén một thư mục:
```bash
7z a archive.7z /path/to/directory
```

- Giải nén một tập tin nén:
```bash
7z x archive.7z
```

- Liệt kê nội dung của tập tin nén:
```bash
7z l archive.7z
```

- Xóa một tập tin từ tập tin nén:
```bash
7z d archive.7z file.txt
```

- Kiểm tra tính toàn vẹn của tập tin nén:
```bash
7z t archive.7z
```

## Mẹo
- Sử dụng tùy chọn `-p` để bảo vệ tập tin nén bằng mật khẩu.
- Để nén nhiều tập tin, bạn có thể sử dụng dấu hoa thị `*` để chọn tất cả các tập tin trong thư mục.
- Luôn kiểm tra tính toàn vẹn của tập tin nén sau khi nén hoặc giải nén để đảm bảo không có lỗi xảy ra.