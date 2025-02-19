# [Hệ điều hành] C Shell (csh) awk Cách sử dụng: Truy vấn và xử lý văn bản

## Tổng quan
Lệnh `awk` là một công cụ mạnh mẽ trong C Shell (csh) dùng để xử lý và phân tích văn bản. Nó cho phép người dùng thực hiện các thao tác trên dữ liệu văn bản, như lọc, định dạng và tính toán.

## Cách sử dụng
Cú pháp cơ bản của lệnh `awk` như sau:

```bash
awk [options] [arguments]
```

## Các tùy chọn phổ biến
- `-F`: Đặt ký tự phân cách trường (field separator).
- `-v`: Gán giá trị cho biến trước khi thực thi.
- `-f`: Chỉ định tệp chứa mã lệnh `awk`.
- `-W`: Sử dụng các tùy chọn đặc biệt.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế sử dụng lệnh `awk`:

1. **In ra cột thứ hai của một tệp:**
   ```bash
   awk '{print $2}' ten_tap.txt
   ```

2. **Tính tổng của cột số:**
   ```bash
   awk '{sum += $1} END {print sum}' ten_tap.txt
   ```

3. **Lọc các dòng có giá trị lớn hơn 100 trong cột thứ nhất:**
   ```bash
   awk '$1 > 100' ten_tap.txt
   ```

4. **Đặt ký tự phân cách là dấu phẩy và in ra cột thứ nhất:**
   ```bash
   awk -F, '{print $1}' ten_tap.csv
   ```

## Mẹo
- Sử dụng tùy chọn `-F` để thay đổi ký tự phân cách nếu dữ liệu của bạn không phải là khoảng trắng.
- Thực hành với các tệp nhỏ trước khi áp dụng cho các tệp lớn để hiểu rõ cách hoạt động của `awk`.
- Kết hợp `awk` với các lệnh khác như `grep` hoặc `sort` để xử lý dữ liệu hiệu quả hơn.