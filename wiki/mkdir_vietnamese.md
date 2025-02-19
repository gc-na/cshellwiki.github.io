# [Hệ điều hành] C Shell (csh) mkdir Cách sử dụng: Tạo thư mục mới

## Tổng quan
Lệnh `mkdir` được sử dụng để tạo thư mục mới trong hệ thống tệp. Đây là một lệnh cơ bản nhưng rất hữu ích trong việc quản lý cấu trúc thư mục.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mkdir` như sau:
```csh
mkdir [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-p`: Tạo các thư mục cha nếu chúng chưa tồn tại.
- `-m`: Đặt quyền truy cập cho thư mục mới được tạo.
- `-v`: Hiển thị thông tin chi tiết về các thư mục đã được tạo.

## Ví dụ phổ biến
Dưới đây là một số ví dụ về cách sử dụng lệnh `mkdir`:

1. Tạo một thư mục đơn giản:
   ```csh
   mkdir myfolder
   ```

2. Tạo nhiều thư mục cùng một lúc:
   ```csh
   mkdir folder1 folder2 folder3
   ```

3. Tạo thư mục cha nếu chưa tồn tại:
   ```csh
   mkdir -p parent/child
   ```

4. Tạo thư mục với quyền truy cập cụ thể:
   ```csh
   mkdir -m 755 mysecurefolder
   ```

5. Hiển thị thông tin khi tạo thư mục:
   ```csh
   mkdir -v newfolder
   ```

## Mẹo
- Luôn kiểm tra xem thư mục đã tồn tại hay chưa trước khi tạo để tránh lỗi.
- Sử dụng tùy chọn `-p` khi bạn không chắc chắn về sự tồn tại của các thư mục cha.
- Đặt quyền truy cập ngay khi tạo thư mục để đảm bảo an toàn và quyền riêng tư.