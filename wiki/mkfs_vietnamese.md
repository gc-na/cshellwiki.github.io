# [Linux] Bash mkfs cách sử dụng: Tạo hệ thống tệp

## Tổng quan
Lệnh `mkfs` (make filesystem) được sử dụng để tạo một hệ thống tệp trên một phân vùng hoặc thiết bị lưu trữ. Nó định dạng thiết bị để có thể lưu trữ dữ liệu theo một cấu trúc nhất định, cho phép hệ điều hành quản lý và truy cập dữ liệu hiệu quả hơn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mkfs` như sau:

```bash
mkfs [options] [arguments]
```

## Các tùy chọn phổ biến
- `-t`: Chỉ định loại hệ thống tệp (ví dụ: ext4, xfs).
- `-L`: Gán nhãn cho hệ thống tệp.
- `-n`: Không thực hiện định dạng, chỉ hiển thị thông tin về hệ thống tệp.
- `-V`: Hiển thị thông tin chi tiết về quá trình tạo hệ thống tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mkfs`:

1. Tạo hệ thống tệp ext4 trên phân vùng `/dev/sdb1`:
   ```bash
   mkfs.ext4 /dev/sdb1
   ```

2. Tạo hệ thống tệp xfs trên phân vùng `/dev/sdc1`:
   ```bash
   mkfs.xfs /dev/sdc1
   ```

3. Gán nhãn cho hệ thống tệp ext4:
   ```bash
   mkfs.ext4 -L mylabel /dev/sdb1
   ```

4. Hiển thị thông tin mà không thực hiện định dạng:
   ```bash
   mkfs.ext4 -n /dev/sdb1
   ```

## Mẹo
- Trước khi sử dụng `mkfs`, hãy chắc chắn rằng bạn đã sao lưu dữ liệu quan trọng, vì quá trình này sẽ xóa tất cả dữ liệu trên phân vùng.
- Kiểm tra phân vùng bằng lệnh `lsblk` để đảm bảo bạn đang định dạng đúng thiết bị.
- Sử dụng tùy chọn `-V` để theo dõi tiến trình và nhận thông tin chi tiết trong quá trình tạo hệ thống tệp.