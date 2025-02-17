# [Linux] Bash sed Cách sử dụng: Thay thế và chỉnh sửa văn bản

## Tổng quan
Lệnh `sed` (stream editor) là một công cụ mạnh mẽ trong Bash dùng để xử lý và chỉnh sửa văn bản trong dòng. Nó cho phép bạn thực hiện các thao tác như thay thế, xóa hoặc chèn văn bản trong các tệp hoặc đầu vào từ dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `sed` như sau:

```bash
sed [options] [arguments]
```

## Các tùy chọn phổ biến
- `-e`: Chỉ định một lệnh `sed` để thực hiện.
- `-i`: Thay đổi trực tiếp tệp mà không cần xuất ra tệp mới.
- `-n`: Ngăn chặn việc in ra tất cả các dòng, chỉ in các dòng được chỉ định.
- `s`: Lệnh thay thế, cho phép thay thế một chuỗi bằng một chuỗi khác.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sed`:

1. **Thay thế một chuỗi trong tệp**:
   ```bash
   sed -i 's/chuỗi_cũ/chuỗi_mới/g' ten_tap.txt
   ```
   Lệnh này sẽ thay thế tất cả các xuất hiện của "chuỗi_cũ" bằng "chuỗi_mới" trong tệp `ten_tap.txt`.

2. **Xóa một dòng chứa chuỗi cụ thể**:
   ```bash
   sed -i '/chuỗi_xóa/d' ten_tap.txt
   ```
   Lệnh này sẽ xóa tất cả các dòng chứa "chuỗi_xóa" trong tệp `ten_tap.txt`.

3. **Chèn một dòng mới sau một dòng cụ thể**:
   ```bash
   sed -i '/chuỗi_tìm/ a Dòng_mới' ten_tap.txt
   ```
   Lệnh này sẽ chèn "Dòng_mới" ngay sau dòng chứa "chuỗi_tìm" trong tệp `ten_tap.txt`.

4. **In ra các dòng chứa chuỗi cụ thể**:
   ```bash
   sed -n '/chuỗi_in/p' ten_tap.txt
   ```
   Lệnh này sẽ chỉ in ra các dòng trong `ten_tap.txt` chứa "chuỗi_in".

## Mẹo
- Sử dụng tùy chọn `-i` với cẩn thận, vì nó sẽ thay đổi tệp gốc mà không có bản sao lưu.
- Bạn có thể sử dụng `-e` để thực hiện nhiều lệnh `sed` trong một lần.
- Để kiểm tra kết quả trước khi thay đổi, hãy bỏ tùy chọn `-i` và xem kết quả trên màn hình.

Hy vọng bài viết này giúp bạn hiểu rõ hơn về cách sử dụng lệnh `sed` trong Bash!