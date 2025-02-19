# [Hệ điều hành] C Shell (csh) mv: Di chuyển hoặc đổi tên tệp

## Overview
Lệnh `mv` trong C Shell (csh) được sử dụng để di chuyển hoặc đổi tên các tệp và thư mục. Khi bạn muốn thay đổi vị trí của một tệp hoặc đơn giản là đổi tên nó, lệnh này sẽ giúp bạn thực hiện điều đó một cách dễ dàng.

## Usage
Cú pháp cơ bản của lệnh `mv` như sau:
```
mv [options] [arguments]
```

## Common Options
- `-i`: Yêu cầu xác nhận trước khi ghi đè lên tệp đã tồn tại.
- `-u`: Chỉ di chuyển tệp nếu tệp nguồn mới hơn tệp đích hoặc nếu tệp đích không tồn tại.
- `-v`: Hiển thị thông tin chi tiết về các tệp đang được di chuyển.

## Common Examples
- Di chuyển một tệp từ thư mục hiện tại đến một thư mục khác:
  ```bash
  mv file.txt /path/to/destination/
  ```

- Đổi tên một tệp:
  ```bash
  mv oldname.txt newname.txt
  ```

- Di chuyển và đổi tên một tệp cùng lúc:
  ```bash
  mv file.txt /path/to/destination/newname.txt
  ```

- Di chuyển nhiều tệp vào một thư mục:
  ```bash
  mv file1.txt file2.txt /path/to/destination/
  ```

- Sử dụng tùy chọn xác nhận trước khi ghi đè:
  ```bash
  mv -i file.txt /path/to/destination/
  ```

## Tips
- Luôn kiểm tra tên tệp và đường dẫn trước khi thực hiện lệnh `mv` để tránh mất dữ liệu.
- Sử dụng tùy chọn `-v` để theo dõi quá trình di chuyển tệp, đặc biệt khi làm việc với nhiều tệp.
- Nếu bạn không chắc chắn về hành động của lệnh, hãy sử dụng tùy chọn `-i` để được nhắc xác nhận trước khi ghi đè lên tệp.