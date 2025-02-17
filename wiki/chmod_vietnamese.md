# [Linux] Bash chmod cách sử dụng: Thay đổi quyền truy cập tệp

## Tổng quan
Lệnh `chmod` trong Bash được sử dụng để thay đổi quyền truy cập cho các tệp và thư mục trong hệ thống tệp. Quyền truy cập có thể được thiết lập cho người sở hữu tệp, nhóm và người dùng khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `chmod` như sau:
```bash
chmod [options] [arguments]
```

## Các tùy chọn phổ biến
- `-R`: Thay đổi quyền truy cập cho tất cả các tệp và thư mục con bên trong thư mục.
- `u`: Đại diện cho người sở hữu tệp (user).
- `g`: Đại diện cho nhóm (group).
- `o`: Đại diện cho người dùng khác (others).
- `a`: Đại diện cho tất cả (all).
- `+`: Thêm quyền.
- `-`: Xóa quyền.
- `=`: Thiết lập quyền cụ thể.

## Ví dụ phổ biến
- Thay đổi quyền cho người sở hữu tệp thành đọc, ghi và thực thi:
```bash
chmod u+rwx filename
```

- Thay đổi quyền cho nhóm thành chỉ đọc:
```bash
chmod g+r filename
```

- Xóa quyền thực thi cho tất cả người dùng:
```bash
chmod a-x filename
```

- Thay đổi quyền cho tất cả tệp trong thư mục hiện tại và thư mục con:
```bash
chmod -R 755 directory_name
```

## Mẹo
- Sử dụng `ls -l` để kiểm tra quyền truy cập hiện tại của tệp trước khi thay đổi.
- Cẩn thận khi sử dụng tùy chọn `-R`, vì nó có thể thay đổi quyền cho nhiều tệp và thư mục không mong muốn.
- Nên sử dụng quyền tối thiểu cần thiết để bảo mật tốt hơn cho hệ thống của bạn.