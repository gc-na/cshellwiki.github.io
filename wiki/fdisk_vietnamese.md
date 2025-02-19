# [Hệ điều hành] C Shell (csh) fdisk Cách sử dụng: Quản lý phân vùng ổ đĩa

## Tổng quan
Lệnh `fdisk` được sử dụng để quản lý phân vùng ổ đĩa trên hệ thống Unix và Linux. Nó cho phép người dùng tạo, xóa, và thay đổi kích thước các phân vùng trên ổ đĩa cứng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `fdisk` như sau:
```
fdisk [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-l`: Liệt kê tất cả các phân vùng trên các ổ đĩa.
- `-u`: Sử dụng đơn vị là megabyte cho các kích thước phân vùng.
- `-n`: Tạo một phân vùng mới.
- `-d`: Xóa một phân vùng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `fdisk`:

1. **Liệt kê các phân vùng trên ổ đĩa**:
   ```bash
   fdisk -l
   ```

2. **Tạo một phân vùng mới**:
   ```bash
   fdisk /dev/sda
   ```
   Sau đó, bạn có thể nhập các lệnh tương ứng trong giao diện tương tác để tạo phân vùng.

3. **Xóa một phân vùng**:
   ```bash
   fdisk /dev/sda
   ```
   Nhập lệnh `d` trong giao diện tương tác và chọn phân vùng cần xóa.

## Mẹo
- Trước khi thực hiện bất kỳ thay đổi nào với `fdisk`, hãy sao lưu dữ liệu quan trọng để tránh mất mát.
- Sử dụng lệnh `man fdisk` để xem hướng dẫn chi tiết và các tùy chọn bổ sung.
- Hãy cẩn thận khi xóa hoặc thay đổi phân vùng, vì điều này có thể ảnh hưởng đến hệ thống và dữ liệu của bạn.