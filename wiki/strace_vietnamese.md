# [Hệ điều hành] C Shell (csh) strace: [theo dõi hệ thống]

## Tổng quan
Lệnh `strace` được sử dụng để theo dõi các cuộc gọi hệ thống và tín hiệu của một chương trình. Nó giúp người dùng hiểu cách mà một chương trình tương tác với hệ điều hành, từ đó hỗ trợ trong việc gỡ lỗi và tối ưu hóa hiệu suất.

## Cú pháp
Cú pháp cơ bản của lệnh `strace` như sau:
```
strace [options] [arguments]
```

## Các tùy chọn phổ biến
- `-c`: Tóm tắt thống kê các cuộc gọi hệ thống.
- `-e expr`: Chỉ theo dõi các cuộc gọi hệ thống được chỉ định bởi biểu thức `expr`.
- `-o filename`: Ghi đầu ra vào tệp được chỉ định thay vì hiển thị trên màn hình.
- `-p pid`: Theo dõi một tiến trình đang chạy với ID tiến trình `pid`.

## Ví dụ phổ biến
- Theo dõi một chương trình đơn giản:
  ```bash
  strace ls
  ```
- Ghi đầu ra vào một tệp:
  ```bash
  strace -o output.txt ls
  ```
- Theo dõi một tiến trình đang chạy:
  ```bash
  strace -p 1234
  ```
- Tóm tắt thống kê các cuộc gọi hệ thống:
  ```bash
  strace -c ls
  ```

## Mẹo
- Sử dụng tùy chọn `-e` để chỉ theo dõi các cuộc gọi hệ thống cụ thể nhằm giảm lượng thông tin đầu ra.
- Ghi lại đầu ra vào tệp để phân tích sau này, đặc biệt khi theo dõi các chương trình phức tạp.
- Kết hợp với các công cụ khác như `grep` để lọc thông tin đầu ra theo nhu cầu.