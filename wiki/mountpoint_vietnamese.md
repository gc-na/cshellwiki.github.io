# [Linux] Bash mountpoint: Kiểm tra điểm gắn kết

## Overview
Lệnh `mountpoint` được sử dụng để xác định xem một thư mục cụ thể có phải là điểm gắn kết của một hệ thống tệp hay không. Điều này rất hữu ích khi bạn muốn kiểm tra trạng thái của các phân vùng hoặc thiết bị đã được gắn kết.

## Usage
Cú pháp cơ bản của lệnh `mountpoint` như sau:

```
mountpoint [options] [arguments]
```

## Common Options
- `-q`: Chạy trong chế độ im lặng, không xuất ra thông tin gì.
- `-n`: Không phân tích cú pháp tên tệp, hữu ích khi làm việc với các tên tệp không chuẩn.

## Common Examples
- Kiểm tra một thư mục có phải là điểm gắn kết hay không:

```bash
mountpoint /mnt/data
```

- Kiểm tra nhiều thư mục cùng lúc:

```bash
mountpoint /mnt/data /mnt/backup
```

- Sử dụng chế độ im lặng để kiểm tra mà không xuất thông tin:

```bash
mountpoint -q /mnt/data
```

## Tips
- Sử dụng lệnh `mountpoint` trong các kịch bản shell để tự động hóa việc kiểm tra trạng thái gắn kết của các phân vùng.
- Kết hợp với các lệnh khác như `if` để thực hiện các hành động khác nhau dựa trên kết quả kiểm tra.