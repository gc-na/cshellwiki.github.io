# [Linux] Bash hexdump Cách sử dụng: Hiển thị nội dung tệp ở định dạng thập lục phân

## Tổng quan
Lệnh `hexdump` trong Bash được sử dụng để hiển thị nội dung của tệp ở định dạng thập lục phân. Nó cho phép người dùng xem các byte của tệp dưới dạng số thập lục phân, giúp phân tích và kiểm tra dữ liệu nhị phân.

## Cách sử dụng
Cú pháp cơ bản của lệnh `hexdump` như sau:

```
hexdump [options] [arguments]
```

## Các tùy chọn phổ biến
- `-C`: Hiển thị nội dung tệp theo định dạng thập lục phân và ASCII.
- `-n <số byte>`: Chỉ hiển thị số byte cụ thể từ tệp.
- `-v`: Hiển thị tất cả các byte, bao gồm cả các byte lặp lại.
- `-e <format>`: Chỉ định định dạng đầu ra tùy chỉnh.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `hexdump`:

1. Hiển thị nội dung tệp ở định dạng thập lục phân:
   ```bash
   hexdump myfile.bin
   ```

2. Hiển thị nội dung tệp với định dạng thập lục phân và ASCII:
   ```bash
   hexdump -C myfile.bin
   ```

3. Chỉ hiển thị 16 byte đầu tiên của tệp:
   ```bash
   hexdump -n 16 myfile.bin
   ```

4. Sử dụng định dạng tùy chỉnh để hiển thị:
   ```bash
   hexdump -e '16/1 "%02x " "\n"' myfile.bin
   ```

## Mẹo
- Sử dụng tùy chọn `-C` để dễ dàng đọc và phân tích dữ liệu, vì nó cung cấp cả định dạng thập lục phân và ASCII.
- Khi làm việc với tệp lớn, hãy sử dụng tùy chọn `-n` để giới hạn số byte được hiển thị, giúp tiết kiệm thời gian và không gian.
- Thử nghiệm với tùy chọn `-e` để tạo định dạng đầu ra tùy chỉnh phù hợp với nhu cầu của bạn.