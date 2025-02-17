# [Linux] Bash hash cách sử dụng: Lưu trữ vị trí của các lệnh

## Tổng quan
Lệnh `hash` trong Bash được sử dụng để quản lý và lưu trữ vị trí của các lệnh đã được thực thi. Khi bạn chạy một lệnh, Bash sẽ ghi nhớ vị trí của nó để tăng tốc độ thực thi trong tương lai. Điều này giúp giảm thiểu thời gian tìm kiếm lệnh khi bạn gọi lại chúng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `hash` như sau:

```bash
hash [options] [arguments]
```

## Các tùy chọn phổ biến
- `-r`: Xóa tất cả các mục trong bảng băm, tức là làm mới bộ nhớ cache của các lệnh.
- `-l`: Hiển thị danh sách các lệnh đã được lưu trữ cùng với vị trí của chúng.
- `-p`: Cung cấp một đường dẫn cụ thể cho lệnh mà bạn muốn lưu trữ.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `hash`:

1. **Hiển thị danh sách các lệnh đã được lưu trữ**:
   ```bash
   hash
   ```

2. **Làm mới bảng băm**:
   ```bash
   hash -r
   ```

3. **Lưu trữ một lệnh với đường dẫn cụ thể**:
   ```bash
   hash -p /usr/local/bin/mycommand mycommand
   ```

4. **Hiển thị vị trí của một lệnh cụ thể**:
   ```bash
   hash mycommand
   ```

## Mẹo
- Sử dụng `hash -r` khi bạn đã cài đặt hoặc gỡ bỏ một lệnh mới để đảm bảo Bash nhận diện đúng vị trí của các lệnh.
- Kiểm tra bảng băm thường xuyên để biết các lệnh nào đang được lưu trữ và vị trí của chúng, điều này giúp bạn quản lý môi trường làm việc hiệu quả hơn.
- Khi sử dụng `hash -p`, hãy chắc chắn rằng đường dẫn bạn cung cấp là chính xác để tránh lỗi khi gọi lệnh.