# [Linux] Bash tac Cách sử dụng: Đảo ngược nội dung tệp

## Tổng quan
Lệnh `tac` trong Bash được sử dụng để hiển thị nội dung của một tệp theo thứ tự ngược lại, tức là dòng cuối cùng sẽ được hiển thị trước tiên và dòng đầu tiên sẽ được hiển thị sau cùng. Lệnh này rất hữu ích khi bạn cần xem xét dữ liệu từ dưới lên trên.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tac` như sau:

```bash
tac [tùy chọn] [tệp tin]
```

## Tùy chọn phổ biến
- `-r`, `--regexp`: Sử dụng biểu thức chính quy để xác định các dòng.
- `-s`, `--separator=CH`: Đặt ký tự phân cách giữa các dòng.
- `-b`, `--before`: Đảo ngược các dòng trước khi phân cách.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `tac`:

1. Đảo ngược nội dung của một tệp tin:
   ```bash
   tac ten_tap_tin.txt
   ```

2. Đảo ngược nội dung và lưu vào một tệp tin mới:
   ```bash
   tac ten_tap_tin.txt > tap_tin_moi.txt
   ```

3. Sử dụng tùy chọn phân cách với ký tự `,`:
   ```bash
   tac -s ',' ten_tap_tin.txt
   ```

4. Đảo ngược nội dung của nhiều tệp tin:
   ```bash
   tac tap_tin_1.txt tap_tin_2.txt
   ```

## Mẹo
- Khi làm việc với các tệp lớn, hãy cân nhắc sử dụng `less` để xem nội dung theo thứ tự ngược lại mà không cần tải toàn bộ tệp vào bộ nhớ.
- Kết hợp `tac` với các lệnh khác như `grep` để lọc nội dung trước khi đảo ngược.
- Sử dụng `tac` để kiểm tra các tệp log, giúp bạn nhanh chóng tìm thấy các sự kiện gần đây nhất.