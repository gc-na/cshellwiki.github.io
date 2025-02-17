# [Linux] Bash ln cách sử dụng: Tạo liên kết giữa các tệp

## Overview
Lệnh `ln` trong Bash được sử dụng để tạo các liên kết giữa các tệp. Có hai loại liên kết chính: liên kết cứng (hard link) và liên kết mềm (symbolic link). Liên kết cứng là một bản sao của tệp gốc, trong khi liên kết mềm là một đường dẫn đến tệp gốc.

## Usage
Cú pháp cơ bản của lệnh `ln` như sau:
```bash
ln [options] [arguments]
```

## Common Options
- `-s`: Tạo liên kết mềm.
- `-f`: Ghi đè lên tệp đích nếu nó đã tồn tại.
- `-n`: Không làm ghi đè lên tệp đích nếu nó là một liên kết.
- `-v`: Hiển thị thông tin chi tiết về các tệp đã được liên kết.

## Common Examples
### Tạo liên kết cứng
```bash
ln file1.txt file2.txt
```
Lệnh này tạo một liên kết cứng từ `file1.txt` đến `file2.txt`.

### Tạo liên kết mềm
```bash
ln -s /path/to/original/file.txt /path/to/link/file_link.txt
```
Lệnh này tạo một liên kết mềm từ tệp gốc `file.txt` đến `file_link.txt`.

### Ghi đè lên liên kết cũ
```bash
ln -f file1.txt file2.txt
```
Lệnh này sẽ ghi đè lên `file2.txt` nếu nó đã tồn tại.

### Hiển thị thông tin chi tiết
```bash
ln -v file1.txt file2.txt
```
Lệnh này sẽ hiển thị thông tin về việc tạo liên kết.

## Tips
- Sử dụng liên kết mềm khi bạn muốn tạo một đường dẫn đến tệp gốc mà không sao chép nội dung.
- Hãy cẩn thận khi sử dụng tùy chọn `-f`, vì nó có thể ghi đè lên các tệp quan trọng.
- Kiểm tra các liên kết bằng cách sử dụng lệnh `ls -l` để đảm bảo rằng chúng đã được tạo chính xác.