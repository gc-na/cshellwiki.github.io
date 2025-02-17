# [Linux] Bash rmdir Cách sử dụng: Xóa thư mục rỗng

## Tổng quan
Lệnh `rmdir` được sử dụng để xóa các thư mục rỗng trong hệ thống tệp. Nếu thư mục không rỗng, lệnh sẽ không thực hiện được và sẽ thông báo lỗi.

## Cách sử dụng
Cú pháp cơ bản của lệnh `rmdir` như sau:
```
rmdir [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-p`: Xóa thư mục rỗng và tất cả các thư mục cha của nó nếu chúng cũng rỗng.
- `--ignore-fail-on-non-empty`: Bỏ qua lỗi nếu thư mục không rỗng.

## Ví dụ phổ biến
- Xóa một thư mục rỗng:
  ```bash
  rmdir my_empty_directory
  ```

- Xóa nhiều thư mục rỗng cùng lúc:
  ```bash
  rmdir dir1 dir2 dir3
  ```

- Xóa thư mục rỗng và các thư mục cha của nó:
  ```bash
  rmdir -p parent_dir/child_dir
  ```

- Bỏ qua lỗi khi thư mục không rỗng:
  ```bash
  rmdir --ignore-fail-on-non-empty my_directory
  ```

## Mẹo
- Trước khi sử dụng `rmdir`, hãy chắc chắn rằng thư mục bạn muốn xóa là rỗng để tránh thông báo lỗi.
- Sử dụng lệnh `ls` để kiểm tra nội dung của thư mục trước khi xóa.
- Để xóa thư mục không rỗng, hãy sử dụng lệnh `rm -r` thay vì `rmdir`.