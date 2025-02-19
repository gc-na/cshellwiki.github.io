# [Hệ điều hành] C Shell (csh) sqlite3 Cách sử dụng: Truy cập và quản lý cơ sở dữ liệu SQLite

## Tổng quan
Lệnh `sqlite3` được sử dụng để truy cập và quản lý cơ sở dữ liệu SQLite. Đây là một công cụ dòng lệnh mạnh mẽ cho phép người dùng thực hiện các truy vấn SQL, tạo và quản lý cơ sở dữ liệu một cách dễ dàng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `sqlite3` như sau:
```
sqlite3 [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-help`: Hiển thị thông tin trợ giúp về lệnh.
- `-version`: Hiển thị phiên bản của SQLite.
- `-init <file>`: Chạy các lệnh SQL từ tệp tin đã chỉ định khi khởi động.
- `-batch`: Chạy trong chế độ không tương tác, không hiển thị thông tin đầu ra.

## Ví dụ thường gặp
1. **Tạo một cơ sở dữ liệu mới:**
   ```bash
   sqlite3 mydatabase.db
   ```

2. **Thực hiện một truy vấn SQL để tạo bảng:**
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

3. **Chèn dữ liệu vào bảng:**
   ```bash
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
   ```

4. **Lấy dữ liệu từ bảng:**
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

5. **Xuất dữ liệu ra tệp tin:**
   ```bash
   sqlite3 mydatabase.db ".output output.txt" ".dump" ".output stdout"
   ```

## Mẹo
- Sử dụng chế độ `-batch` khi bạn muốn chạy nhiều lệnh mà không cần tương tác.
- Luôn sao lưu cơ sở dữ liệu trước khi thực hiện các thay đổi lớn.
- Sử dụng lệnh `.tables` để xem danh sách các bảng trong cơ sở dữ liệu hiện tại.