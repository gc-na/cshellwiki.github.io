# [Linux] Bash psql Cách sử dụng: Giao diện dòng lệnh cho PostgreSQL

## Tổng quan
Lệnh `psql` là một công cụ giao diện dòng lệnh cho PostgreSQL, cho phép người dùng tương tác với cơ sở dữ liệu PostgreSQL. Với `psql`, bạn có thể thực hiện các truy vấn SQL, quản lý cơ sở dữ liệu và thực hiện nhiều tác vụ khác liên quan đến dữ liệu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `psql` như sau:

```bash
psql [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-h, --host=HOST`: Chỉ định địa chỉ máy chủ nơi cơ sở dữ liệu đang chạy.
- `-p, --port=PORT`: Chỉ định cổng mà máy chủ PostgreSQL đang lắng nghe.
- `-U, --username=USERNAME`: Chỉ định tên người dùng để kết nối đến cơ sở dữ liệu.
- `-d, --dbname=DBNAME`: Chỉ định tên cơ sở dữ liệu mà bạn muốn kết nối.
- `-f, --file=FILE`: Thực thi các lệnh SQL từ tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `psql`.

### Kết nối đến cơ sở dữ liệu
```bash
psql -U username -d dbname
```

### Thực thi một tệp SQL
```bash
psql -U username -d dbname -f script.sql
```

### Xuất dữ liệu từ bảng
```bash
psql -U username -d dbname -c "SELECT * FROM tablename;"
```

### Kết nối đến máy chủ từ xa
```bash
psql -h remote_host -U username -d dbname
```

## Mẹo
- Sử dụng tùy chọn `-W` để yêu cầu nhập mật khẩu khi kết nối.
- Bạn có thể sử dụng `\?` trong `psql` để xem danh sách các lệnh và tùy chọn có sẵn.
- Để thoát khỏi `psql`, bạn có thể gõ `\q`.