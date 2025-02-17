# [Linux] Bash rev: Đảo ngược chuỗi ký tự

## Overview
Lệnh `rev` trong Bash được sử dụng để đảo ngược thứ tự các ký tự trong mỗi dòng của đầu vào. Điều này có nghĩa là nếu bạn có một chuỗi văn bản, lệnh này sẽ biến nó thành một chuỗi với các ký tự được sắp xếp ngược lại.

## Usage
Cú pháp cơ bản của lệnh `rev` như sau:
```
rev [options] [arguments]
```

## Common Options
- `-o, --output=FILE`: Ghi kết quả vào tệp FILE thay vì xuất ra màn hình.
- `-h, --help`: Hiển thị thông tin trợ giúp về lệnh `rev`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `rev`.

### Ví dụ 1: Đảo ngược một chuỗi
```bash
echo "Hello World" | rev
```
Kết quả:
```
dlroW olleH
```

### Ví dụ 2: Đảo ngược nội dung của một tệp
Giả sử bạn có một tệp tên là `example.txt` chứa nội dung sau:
```
Hello
World
```
Bạn có thể sử dụng lệnh sau để đảo ngược nội dung của nó:
```bash
rev example.txt
```
Kết quả:
```
olleH
dlroW
```

### Ví dụ 3: Ghi kết quả vào một tệp khác
```bash
rev example.txt > reversed.txt
```
Nội dung của tệp `reversed.txt` sẽ là:
```
olleH
dlroW
```

## Tips
- Sử dụng lệnh `rev` kết hợp với các lệnh khác như `cat`, `echo`, hoặc `grep` để xử lý văn bản một cách linh hoạt hơn.
- Nếu bạn cần đảo ngược nhiều tệp, bạn có thể sử dụng dấu sao (*) để chọn nhiều tệp cùng lúc.
- Hãy kiểm tra kết quả đầu ra trước khi ghi vào tệp để đảm bảo rằng bạn có được kết quả như mong muốn.