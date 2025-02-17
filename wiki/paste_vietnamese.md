# [Linux] Bash paste cách sử dụng: Nối các tệp theo hàng

## Tổng quan
Lệnh `paste` trong Bash được sử dụng để nối các tệp lại với nhau theo hàng. Nó cho phép bạn kết hợp nội dung của nhiều tệp thành một tệp duy nhất, với mỗi tệp được hiển thị trên một hàng riêng biệt.

## Cách sử dụng
Cú pháp cơ bản của lệnh `paste` như sau:
```bash
paste [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-d`: Chỉ định ký tự phân cách giữa các trường (mặc định là tab).
- `-s`: Nối các dòng trong cùng một tệp thành một dòng duy nhất.
- `-z`: Xử lý các tệp như là các chuỗi null-terminated.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `paste`:

1. Nối hai tệp `file1.txt` và `file2.txt`:
   ```bash
   paste file1.txt file2.txt
   ```

2. Sử dụng ký tự phân cách là dấu phẩy:
   ```bash
   paste -d ',' file1.txt file2.txt
   ```

3. Nối nội dung của một tệp thành một dòng duy nhất:
   ```bash
   paste -s file1.txt
   ```

4. Nối nhiều tệp và sử dụng ký tự phân cách là dấu chấm phẩy:
   ```bash
   paste -d ';' file1.txt file2.txt file3.txt
   ```

## Mẹo
- Khi làm việc với nhiều tệp, hãy chắc chắn rằng số lượng dòng trong các tệp là tương đương để tránh mất dữ liệu.
- Sử dụng tùy chọn `-d` để tùy chỉnh ký tự phân cách giúp dễ dàng đọc hơn.
- Kiểm tra kết quả đầu ra bằng cách sử dụng lệnh `less` hoặc `more` để xem nội dung được nối một cách dễ dàng.