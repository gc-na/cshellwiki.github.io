# [Linux] Bash unxz cách sử dụng: Giải nén tệp tin .xz

## Tổng quan
Lệnh `unxz` được sử dụng để giải nén các tệp tin có định dạng .xz, một định dạng nén phổ biến. Lệnh này giúp bạn khôi phục lại tệp tin gốc từ tệp tin nén, tiết kiệm không gian lưu trữ và dễ dàng chia sẻ dữ liệu.

## Cách sử dụng
Cú pháp cơ bản của lệnh `unxz` như sau:

```bash
unxz [tùy chọn] [tệp tin]
```

## Tùy chọn phổ biến
- `-k`, `--keep`: Giữ lại tệp tin nén sau khi giải nén.
- `-f`, `--force`: Buộc giải nén ngay cả khi tệp tin đích đã tồn tại.
- `-v`, `--verbose`: Hiển thị thông tin chi tiết trong quá trình giải nén.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `unxz`:

1. Giải nén một tệp tin .xz:
   ```bash
   unxz file.xz
   ```

2. Giải nén và giữ lại tệp tin nén:
   ```bash
   unxz -k file.xz
   ```

3. Giải nén một tệp tin và buộc ghi đè nếu tệp tin đích đã tồn tại:
   ```bash
   unxz -f file.xz
   ```

4. Giải nén nhiều tệp tin cùng lúc:
   ```bash
   unxz file1.xz file2.xz file3.xz
   ```

5. Hiển thị thông tin chi tiết trong quá trình giải nén:
   ```bash
   unxz -v file.xz
   ```

## Mẹo
- Luôn kiểm tra dung lượng đĩa trước khi giải nén, đặc biệt với các tệp tin lớn.
- Sử dụng tùy chọn `-k` nếu bạn muốn giữ lại tệp tin nén để sử dụng sau này.
- Đọc kỹ thông báo lỗi nếu lệnh không thực hiện thành công, điều này có thể giúp bạn xác định vấn đề nhanh chóng.