# [Linux] Bash echo cách sử dụng: In ra văn bản hoặc biến

## Tổng quan
Lệnh `echo` trong Bash được sử dụng để in ra văn bản hoặc giá trị của các biến ra màn hình. Đây là một trong những lệnh cơ bản và thường được sử dụng trong lập trình shell để hiển thị thông tin cho người dùng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `echo` như sau:
```
echo [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-n`: Không in ra dòng mới sau khi in xong.
- `-e`: Kích hoạt các ký tự thoát (escape characters) như `\n` (dòng mới), `\t` (tab).
- `-E`: Không kích hoạt các ký tự thoát (mặc định).

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `echo`:

1. In ra một chuỗi văn bản đơn giản:
   ```bash
   echo "Chào mừng bạn đến với Bash!"
   ```

2. In ra giá trị của một biến:
   ```bash
   tên="Nguyễn Văn A"
   echo "Xin chào, $tên!"
   ```

3. In ra văn bản mà không có dòng mới:
   ```bash
   echo -n "Đang tải..."
   ```

4. Sử dụng ký tự thoát để định dạng:
   ```bash
   echo -e "Dòng 1\nDòng 2\nDòng 3"
   ```

## Mẹo
- Sử dụng `-n` khi bạn không muốn có dòng mới, điều này hữu ích khi bạn muốn in nhiều thông tin trên cùng một dòng.
- Khi sử dụng ký tự thoát với `-e`, hãy chắc chắn rằng bạn đã kiểm tra kết quả để đảm bảo định dạng như mong muốn.
- Để in ra các ký tự đặc biệt như dấu `$`, bạn có thể sử dụng dấu `\` để thoát, ví dụ: `echo "Giá trị là \$100"` sẽ in ra "Giá trị là $100".