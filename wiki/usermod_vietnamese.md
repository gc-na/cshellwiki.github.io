# [Linux] Bash usermod <Sử dụng người dùng>: Thay đổi thông tin người dùng

## Tổng quan
Lệnh `usermod` trong Bash được sử dụng để thay đổi thông tin của một người dùng đã tồn tại trên hệ thống. Bạn có thể thay đổi tên người dùng, nhóm, thư mục chính, và nhiều thuộc tính khác của tài khoản người dùng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `usermod` như sau:

```bash
usermod [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-l, --login TÊN_MỚI`: Đổi tên đăng nhập của người dùng.
- `-d, --home THƯ_MỤC_MỚI`: Thay đổi thư mục chính của người dùng.
- `-m, --move-home`: Di chuyển thư mục chính đến vị trí mới.
- `-G, --groups NHÓM`: Thêm người dùng vào một hoặc nhiều nhóm.
- `-a, --append`: Thêm người dùng vào nhóm mà không xóa khỏi nhóm hiện tại.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `usermod`:

1. Đổi tên đăng nhập của người dùng từ `olduser` thành `newuser`:
   ```bash
   usermod -l newuser olduser
   ```

2. Thay đổi thư mục chính của người dùng `username` thành `/home/newhome`:
   ```bash
   usermod -d /home/newhome username
   ```

3. Di chuyển thư mục chính của người dùng `username` đến vị trí mới:
   ```bash
   usermod -m -d /home/newhome username
   ```

4. Thêm người dùng `username` vào nhóm `developers`:
   ```bash
   usermod -a -G developers username
   ```

## Mẹo
- Luôn sao lưu dữ liệu quan trọng trước khi thực hiện thay đổi với lệnh `usermod`.
- Kiểm tra các nhóm hiện tại của người dùng bằng lệnh `groups username` trước khi thêm vào nhóm mới.
- Sử dụng lệnh `passwd username` để thay đổi mật khẩu của người dùng sau khi thực hiện thay đổi thông tin.