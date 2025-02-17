# [Linux] Bash sqlite3 Cách sử dụng: Truy cập và quản lý cơ sở dữ liệu SQLite

## Overview
Lệnh `sqlite3` cho phép người dùng tương tác với cơ sở dữ liệu SQLite từ dòng lệnh. Nó cung cấp một giao diện để thực hiện các truy vấn SQL, quản lý cơ sở dữ liệu và thực hiện các thao tác khác liên quan đến dữ liệu.

## Usage
Cú pháp cơ bản của lệnh `sqlite3` như sau:
```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Hiển thị thông tin trợ giúp về lệnh.
- `-version`: Hiển thị phiên bản của SQLite.
- `-init <file>`: Chạy một tệp SQL khi khởi động.
- `-batch`: Chạy trong chế độ không tương tác, không hiển thị thông báo.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `sqlite3`:

1. **Tạo một cơ sở dữ liệu mới**:
   ```bash
   sqlite3 mydatabase.db
   ```

2. **Chạy một tệp SQL**:
   ```bash
   sqlite3 mydatabase.db < script.sql
   ```

3. **Tạo một bảng mới**:
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

4. **Chèn dữ liệu vào bảng**:
   ```bash
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Nguyen Van A');"
   ```

5. **Truy vấn dữ liệu từ bảng**:
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

## Tips
- Sử dụng tùy chọn `-batch` khi bạn muốn chạy nhiều lệnh mà không cần tương tác.
- Luôn sao lưu cơ sở dữ liệu trước khi thực hiện các thao tác thay đổi lớn.
- Tìm hiểu cú pháp SQL để tận dụng tối đa khả năng của `sqlite3`.