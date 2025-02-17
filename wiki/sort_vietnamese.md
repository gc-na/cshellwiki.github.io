# [Linux] Bash sort cách sử dụng: Sắp xếp dữ liệu trong tệp tin

## Overview
Lệnh `sort` trong Bash được sử dụng để sắp xếp các dòng trong một tệp tin hoặc đầu vào từ dòng lệnh theo thứ tự nhất định. Lệnh này rất hữu ích trong việc tổ chức dữ liệu và tìm kiếm thông tin một cách dễ dàng hơn.

## Usage
Cú pháp cơ bản của lệnh `sort` như sau:
```
sort [options] [arguments]
```

## Common Options
- `-r`: Sắp xếp theo thứ tự ngược lại (giảm dần).
- `-n`: Sắp xếp theo giá trị số.
- `-k`: Chỉ định cột để sắp xếp.
- `-u`: Chỉ giữ lại các dòng duy nhất (không trùng lặp).
- `-o`: Ghi kết quả vào tệp tin thay vì xuất ra màn hình.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sort`:

1. **Sắp xếp một tệp tin theo thứ tự tăng dần:**
   ```bash
   sort filename.txt
   ```

2. **Sắp xếp một tệp tin theo thứ tự giảm dần:**
   ```bash
   sort -r filename.txt
   ```

3. **Sắp xếp theo giá trị số:**
   ```bash
   sort -n numbers.txt
   ```

4. **Sắp xếp theo cột thứ hai trong tệp:**
   ```bash
   sort -k 2 filename.txt
   ```

5. **Sắp xếp và ghi kết quả vào một tệp mới:**
   ```bash
   sort filename.txt -o sorted.txt
   ```

6. **Sắp xếp và loại bỏ các dòng trùng lặp:**
   ```bash
   sort -u filename.txt
   ```

## Tips
- Hãy chắc chắn rằng tệp tin bạn muốn sắp xếp không bị khóa hoặc đang được sử dụng bởi một chương trình khác.
- Sử dụng tùy chọn `-o` để ghi kết quả vào tệp mới, giúp bạn giữ nguyên tệp gốc.
- Khi làm việc với dữ liệu lớn, hãy cân nhắc sử dụng các tùy chọn phù hợp để tối ưu hóa hiệu suất.