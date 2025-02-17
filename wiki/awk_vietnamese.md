# [Linux] Bash awk cách sử dụng: Trình xử lý văn bản mạnh mẽ

## Tổng quan
`awk` là một công cụ mạnh mẽ trong Bash dùng để xử lý và phân tích văn bản. Nó cho phép người dùng thực hiện các thao tác như lọc, định dạng và tính toán trên dữ liệu văn bản, đặc biệt là trên các tệp tin có cấu trúc như CSV hoặc TSV.

## Cách sử dụng
Cú pháp cơ bản của lệnh `awk` như sau:

```bash
awk [options] 'pattern { action }' [file]
```

## Tùy chọn phổ biến
- `-F`: Chỉ định ký tự phân cách (delimiter) giữa các trường.
- `-v`: Đặt giá trị cho biến trước khi thực thi.
- `-f`: Chỉ định tệp tin chứa mã lệnh `awk`.
- `NR`: Biến hệ thống đại diện cho số dòng hiện tại.
- `NF`: Biến hệ thống đại diện cho số trường trong dòng hiện tại.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng `awk`:

1. **In ra cột thứ hai của tệp tin:**
   ```bash
   awk '{print $2}' filename.txt
   ```

2. **Lọc các dòng có giá trị lớn hơn 50 trong cột thứ nhất:**
   ```bash
   awk '$1 > 50' filename.txt
   ```

3. **Tính tổng giá trị trong cột thứ ba:**
   ```bash
   awk '{sum += $3} END {print sum}' filename.txt
   ```

4. **Đặt ký tự phân cách là dấu phẩy và in ra cột đầu tiên:**
   ```bash
   awk -F, '{print $1}' filename.csv
   ```

5. **Sử dụng biến để lọc:**
   ```bash
   awk -v threshold=100 '$1 > threshold' filename.txt
   ```

## Mẹo
- Sử dụng `-F` để dễ dàng làm việc với các tệp tin có định dạng khác nhau.
- Kết hợp `awk` với các lệnh khác như `grep` hoặc `sort` để xử lý dữ liệu hiệu quả hơn.
- Thử nghiệm với các mẫu và hành động khác nhau để khám phá sức mạnh của `awk`.