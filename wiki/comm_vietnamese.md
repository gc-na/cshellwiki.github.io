# [Hệ điều hành] C Shell (csh) comm: So sánh hai tệp tin

## Overview
Lệnh `comm` trong C Shell (csh) được sử dụng để so sánh hai tệp tin đã được sắp xếp và hiển thị các dòng khác nhau giữa chúng. Nó phân chia kết quả thành ba cột: dòng chỉ có trong tệp đầu tiên, dòng chỉ có trong tệp thứ hai, và dòng có trong cả hai tệp.

## Usage
Cú pháp cơ bản của lệnh `comm` như sau:
```
comm [options] [arguments]
```

## Common Options
- `-1`: Không hiển thị cột đầu tiên (dòng chỉ có trong tệp đầu tiên).
- `-2`: Không hiển thị cột thứ hai (dòng chỉ có trong tệp thứ hai).
- `-3`: Không hiển thị cột thứ ba (dòng có trong cả hai tệp).
- `-i`: Bỏ qua sự khác biệt về chữ hoa và chữ thường khi so sánh.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `comm`:

1. So sánh hai tệp tin đã được sắp xếp:
   ```bash
   comm file1.txt file2.txt
   ```

2. Chỉ hiển thị các dòng chỉ có trong `file1.txt`:
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. Chỉ hiển thị các dòng chỉ có trong `file2.txt`:
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. So sánh hai tệp tin mà không phân biệt chữ hoa và chữ thường:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- Đảm bảo rằng cả hai tệp tin được sắp xếp trước khi sử dụng lệnh `comm`, nếu không kết quả sẽ không chính xác.
- Sử dụng các tùy chọn để tùy chỉnh đầu ra theo nhu cầu của bạn, giúp dễ dàng phân tích kết quả hơn.
- Kết hợp lệnh `comm` với các lệnh khác như `sort` để xử lý dữ liệu một cách hiệu quả hơn.