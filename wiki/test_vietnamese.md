# [Linux] Bash test lệnh: Kiểm tra điều kiện

## Overview
Lệnh `test` trong Bash được sử dụng để kiểm tra điều kiện và trả về mã trạng thái. Nó thường được sử dụng trong các câu lệnh điều kiện để xác định xem một điều kiện có đúng hay không.

## Usage
Cú pháp cơ bản của lệnh `test` như sau:
```bash
test [options] [arguments]
```

## Common Options
- `-e FILE`: Kiểm tra xem tệp có tồn tại hay không.
- `-d FILE`: Kiểm tra xem tệp có phải là thư mục hay không.
- `-f FILE`: Kiểm tra xem tệp có phải là tệp thường hay không.
- `-z STRING`: Kiểm tra xem chuỗi có rỗng hay không.
- `-n STRING`: Kiểm tra xem chuỗi có không rỗng hay không.
- `STRING1 = STRING2`: Kiểm tra xem hai chuỗi có bằng nhau hay không.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `test`:

1. Kiểm tra xem một tệp có tồn tại hay không:
   ```bash
   test -e /path/to/file && echo "Tệp tồn tại"
   ```

2. Kiểm tra xem một thư mục có tồn tại hay không:
   ```bash
   test -d /path/to/directory && echo "Thư mục tồn tại"
   ```

3. Kiểm tra xem một tệp có phải là tệp thường hay không:
   ```bash
   test -f /path/to/file && echo "Đây là tệp thường"
   ```

4. Kiểm tra xem một chuỗi có rỗng hay không:
   ```bash
   STRING=""
   test -z "$STRING" && echo "Chuỗi rỗng"
   ```

5. So sánh hai chuỗi:
   ```bash
   STRING1="Hello"
   STRING2="World"
   test "$STRING1" = "$STRING2" && echo "Hai chuỗi bằng nhau" || echo "Hai chuỗi khác nhau"
   ```

## Tips
- Sử dụng `[[ ... ]]` thay vì `test` để có cú pháp dễ đọc hơn và hỗ trợ thêm các tính năng như so sánh chuỗi.
- Kết hợp lệnh `test` với các câu lệnh điều kiện trong Bash như `if` để thực hiện các hành động dựa trên kết quả kiểm tra.
- Luôn kiểm tra mã trạng thái của lệnh `test` để xử lý các tình huống khác nhau trong kịch bản của bạn.