# [Linux] Bash zip cách sử dụng: Nén và lưu trữ tệp tin

## Overview
Lệnh `zip` được sử dụng để nén và lưu trữ các tệp tin trong một tệp zip. Điều này giúp tiết kiệm không gian lưu trữ và dễ dàng chia sẻ tệp tin qua mạng.

## Usage
Cú pháp cơ bản của lệnh zip như sau:
```bash
zip [options] [arguments]
```

## Common Options
- `-r`: Nén thư mục và tất cả các tệp bên trong.
- `-e`: Mã hóa tệp zip bằng mật khẩu.
- `-u`: Cập nhật các tệp đã có trong tệp zip.
- `-d`: Xóa tệp từ tệp zip.
- `-l`: Liệt kê nội dung của tệp zip.

## Common Examples
1. **Nén một tệp tin**:
   ```bash
   zip myarchive.zip file1.txt
   ```

2. **Nén nhiều tệp tin**:
   ```bash
   zip myarchive.zip file1.txt file2.txt file3.txt
   ```

3. **Nén một thư mục và tất cả các tệp bên trong**:
   ```bash
   zip -r myarchive.zip myfolder/
   ```

4. **Mã hóa tệp zip bằng mật khẩu**:
   ```bash
   zip -e myarchive.zip file1.txt
   ```

5. **Cập nhật tệp trong tệp zip**:
   ```bash
   zip -u myarchive.zip file1.txt
   ```

6. **Xóa tệp từ tệp zip**:
   ```bash
   zip -d myarchive.zip file1.txt
   ```

## Tips
- Sử dụng tùy chọn `-r` để nén toàn bộ thư mục một cách dễ dàng.
- Đảm bảo rằng bạn nhớ mật khẩu nếu sử dụng tùy chọn `-e`, vì không thể khôi phục tệp nếu quên mật khẩu.
- Kiểm tra nội dung của tệp zip bằng tùy chọn `-l` trước khi giải nén để biết rõ những gì có trong tệp.