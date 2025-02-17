# [Linux] Bash dirs cách sử dụng: Quản lý danh sách thư mục

## Tổng quan
Lệnh `dirs` trong Bash được sử dụng để hiển thị danh sách các thư mục hiện tại trong ngăn xếp thư mục. Nó cho phép người dùng theo dõi và quản lý các thư mục mà họ đã truy cập trong phiên làm việc của mình.

## Cách sử dụng
Cú pháp cơ bản của lệnh `dirs` như sau:
```
dirs [options] [arguments]
```

## Tùy chọn phổ biến
- `-l`: Hiển thị danh sách thư mục theo định dạng dài.
- `-p`: Hiển thị danh sách thư mục mà không có bất kỳ thay đổi nào trong ngăn xếp.
- `+N`: Hiển thị thư mục tại vị trí N trong ngăn xếp.
- `-N`: Hiển thị thư mục tại vị trí N từ cuối ngăn xếp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `dirs`:

1. Hiển thị danh sách thư mục hiện tại:
   ```bash
   dirs
   ```

2. Hiển thị danh sách thư mục theo định dạng dài:
   ```bash
   dirs -l
   ```

3. Hiển thị thư mục ở vị trí thứ hai trong ngăn xếp:
   ```bash
   dirs +2
   ```

4. Hiển thị thư mục ở vị trí thứ nhất từ cuối ngăn xếp:
   ```bash
   dirs -1
   ```

## Mẹo
- Sử dụng `pushd` và `popd` để thay đổi thư mục và tự động cập nhật ngăn xếp thư mục, giúp bạn dễ dàng quản lý các thư mục.
- Thường xuyên kiểm tra danh sách thư mục với `dirs` để tránh nhầm lẫn về vị trí hiện tại trong hệ thống tệp.
- Kết hợp `dirs` với các lệnh khác như `cd` để tối ưu hóa quy trình làm việc của bạn.