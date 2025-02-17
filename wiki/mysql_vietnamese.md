# [Linux] Bash mysql cách sử dụng: Truy cập và quản lý cơ sở dữ liệu MySQL

## Tổng quan
Lệnh `mysql` là một công cụ dòng lệnh cho phép người dùng truy cập và quản lý cơ sở dữ liệu MySQL. Nó cho phép thực hiện các truy vấn SQL, quản lý người dùng, và thực hiện nhiều tác vụ khác liên quan đến cơ sở dữ liệu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mysql` như sau:
```bash
mysql [options] [arguments]
```

## Các tùy chọn phổ biến
- `-u [username]`: Chỉ định tên người dùng để đăng nhập vào MySQL.
- `-p`: Yêu cầu nhập mật khẩu cho người dùng đã chỉ định.
- `-h [hostname]`: Chỉ định máy chủ MySQL (mặc định là localhost).
- `-D [database]`: Chỉ định cơ sở dữ liệu cần sử dụng ngay khi đăng nhập.
- `-e "[query]"`: Thực thi một truy vấn SQL ngay từ dòng lệnh.

## Ví dụ phổ biến
1. **Đăng nhập vào MySQL với tên người dùng và mật khẩu**:
   ```bash
   mysql -u root -p
   ```

2. **Kết nối đến một cơ sở dữ liệu cụ thể**:
   ```bash
   mysql -u root -p -D my_database
   ```

3. **Thực thi một truy vấn SQL từ dòng lệnh**:
   ```bash
   mysql -u root -p -e "SHOW DATABASES;"
   ```

4. **Xuất dữ liệu từ một bảng**:
   ```bash
   mysql -u root -p -D my_database -e "SELECT * FROM my_table;"
   ```

5. **Nhập dữ liệu từ một tệp SQL**:
   ```bash
   mysql -u root -p my_database < my_script.sql
   ```

## Mẹo
- **Sử dụng tệp cấu hình**: Bạn có thể lưu thông tin đăng nhập trong tệp cấu hình `~/.my.cnf` để không phải nhập mật khẩu mỗi lần.
- **Tạo bản sao lưu**: Sử dụng lệnh `mysqldump` để tạo bản sao lưu cho cơ sở dữ liệu của bạn.
- **Sử dụng `--verbose`**: Thêm tùy chọn này để nhận thông tin chi tiết về các truy vấn đang được thực thi.
- **Thực hiện kiểm tra**: Trước khi thực hiện các thay đổi lớn, hãy kiểm tra các truy vấn trong môi trường thử nghiệm để tránh mất dữ liệu.