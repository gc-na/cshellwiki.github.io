# [Linux] Bash awk sử dụng: Trích xuất và xử lý văn bản

## Overview
`awk` là một công cụ mạnh mẽ trong Bash, được sử dụng để xử lý và phân tích văn bản. Nó cho phép người dùng thực hiện các thao tác trên dữ liệu văn bản, như tìm kiếm, lọc và định dạng thông tin từ các tệp hoặc đầu ra của các lệnh khác.

## Usage
Cú pháp cơ bản của lệnh `awk` như sau:
```bash
awk [options] [arguments]
```

## Common Options
- `-F`: Chỉ định ký tự phân cách (delimiter) cho các trường trong dòng.
- `-v`: Đặt giá trị cho biến trước khi thực hiện lệnh awk.
- `-f`: Chạy một tập lệnh awk từ một tệp.

## Common Examples
Dưới đây là một số ví dụ thường gặp khi sử dụng lệnh `awk`:

1. **In ra cột thứ hai từ một tệp:**
   ```bash
   awk '{print $2}' filename.txt
   ```

2. **Sử dụng ký tự phân cách khác:**
   ```bash
   awk -F, '{print $1}' filename.csv
   ```

3. **Tính tổng của cột số:**
   ```bash
   awk '{sum += $1} END {print sum}' numbers.txt
   ```

4. **Lọc các dòng có giá trị lớn hơn một số nhất định:**
   ```bash
   awk '$1 > 100' data.txt
   ```

5. **Chạy một tập lệnh awk từ tệp:**
   ```bash
   awk -f script.awk input.txt
   ```

## Tips
- Sử dụng `-F` để dễ dàng làm việc với các tệp CSV hoặc TSV.
- Thử nghiệm với các biến để tối ưu hóa các lệnh awk phức tạp hơn.
- Sử dụng `print` để định dạng đầu ra theo cách bạn muốn, như thêm văn bản hoặc định dạng số.