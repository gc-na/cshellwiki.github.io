# [Hệ điều hành] C Shell (csh) gunzip Cách sử dụng: Giải nén tệp tin nén

## Tổng quan
Lệnh `gunzip` được sử dụng để giải nén các tệp tin nén có định dạng `.gz`. Nó giúp bạn phục hồi các tệp tin về trạng thái ban đầu của chúng sau khi đã nén.

## Cách sử dụng
Cú pháp cơ bản của lệnh `gunzip` như sau:
```
gunzip [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-c`: Giải nén tệp tin và xuất kết quả ra chuẩn (standard output) mà không xóa tệp tin gốc.
- `-f`: Buộc giải nén, ngay cả khi tệp tin đã tồn tại.
- `-k`: Giữ lại tệp tin gốc sau khi giải nén.
- `-r`: Giải nén tất cả các tệp tin trong thư mục con.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `gunzip`:

1. Giải nén một tệp tin đơn:
   ```bash
   gunzip file.txt.gz
   ```

2. Giải nén và giữ lại tệp tin gốc:
   ```bash
   gunzip -k file.txt.gz
   ```

3. Giải nén tất cả các tệp tin trong thư mục:
   ```bash
   gunzip *.gz
   ```

4. Giải nén và xuất ra chuẩn mà không xóa tệp tin gốc:
   ```bash
   gunzip -c file.txt.gz > file.txt
   ```

## Mẹo
- Hãy luôn kiểm tra dung lượng ổ đĩa trước khi giải nén để đảm bảo có đủ không gian lưu trữ cho tệp tin đã giải nén.
- Sử dụng tùy chọn `-k` nếu bạn muốn giữ lại tệp tin nén để sử dụng sau này.
- Để giải nén tệp tin trong thư mục con, hãy sử dụng tùy chọn `-r` để tiết kiệm thời gian.