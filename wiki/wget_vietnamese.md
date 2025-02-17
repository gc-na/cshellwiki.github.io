# [Linux] Bash wget cách sử dụng: Tải xuống tệp từ Internet

## Tổng quan
Lệnh `wget` là một công cụ dòng lệnh mạnh mẽ được sử dụng để tải xuống tệp từ Internet. Nó hỗ trợ nhiều giao thức như HTTP, HTTPS và FTP, cho phép người dùng tải xuống tệp một cách dễ dàng và hiệu quả.

## Cách sử dụng
Cú pháp cơ bản của lệnh `wget` như sau:

```bash
wget [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-O [tên_tệp]`: Chỉ định tên tệp để lưu khi tải xuống.
- `-c`: Tiếp tục tải xuống một tệp đã bị gián đoạn.
- `-q`: Chạy trong chế độ im lặng, không hiển thị thông tin tải xuống.
- `--limit-rate=[tốc độ]`: Giới hạn tốc độ tải xuống.
- `-r`: Tải xuống một trang web và tất cả các tệp liên quan.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng `wget`:

1. Tải xuống một tệp từ URL:
   ```bash
   wget https://example.com/file.zip
   ```

2. Tải xuống và lưu với tên khác:
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. Tiếp tục tải xuống tệp đã bị gián đoạn:
   ```bash
   wget -c https://example.com/file.zip
   ```

4. Tải xuống một trang web và tất cả các tệp liên quan:
   ```bash
   wget -r https://example.com
   ```

5. Giới hạn tốc độ tải xuống:
   ```bash
   wget --limit-rate=200k https://example.com/file.zip
   ```

## Mẹo
- Sử dụng tùy chọn `-q` để tải xuống mà không làm phiền với thông báo không cần thiết.
- Khi tải xuống nhiều tệp, hãy xem xét sử dụng `-i [tệp]` để chỉ định một tệp chứa danh sách các URL.
- Kiểm tra các tùy chọn khác của `wget` bằng cách sử dụng `man wget` để tìm hiểu thêm về các tính năng nâng cao.