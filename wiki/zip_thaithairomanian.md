# [Linux] Bash zip sử dụng: Nén tệp tin

## Overview
Lệnh `zip` được sử dụng để nén các tệp tin và thư mục thành một tệp zip, giúp tiết kiệm không gian lưu trữ và dễ dàng chia sẻ.

## Usage
Cú pháp cơ bản của lệnh zip như sau:
```
zip [options] [arguments]
```

## Common Options
- `-r`: Nén thư mục và tất cả các tệp con.
- `-e`: Mã hóa tệp zip bằng mật khẩu.
- `-u`: Cập nhật tệp zip bằng cách thêm tệp mới hoặc thay thế tệp đã có.
- `-d`: Xóa tệp từ tệp zip.

## Common Examples
- Nén một tệp:
  ```bash
  zip myarchive.zip myfile.txt
  ```

- Nén một thư mục:
  ```bash
  zip -r myarchive.zip myfolder/
  ```

- Nén nhiều tệp:
  ```bash
  zip myarchive.zip file1.txt file2.txt file3.txt
  ```

- Cập nhật tệp zip:
  ```bash
  zip -u myarchive.zip newfile.txt
  ```

- Xóa tệp khỏi tệp zip:
  ```bash
  zip -d myarchive.zip myfile.txt
  ```

## Tips
- Sử dụng tùy chọn `-e` để bảo vệ tệp zip bằng mật khẩu nếu bạn chia sẻ nó với người khác.
- Kiểm tra nội dung của tệp zip bằng lệnh `unzip -l myarchive.zip` trước khi giải nén.
- Để nén tệp tin mà không cần tạo tệp zip mới, hãy sử dụng tùy chọn `-u` để cập nhật tệp zip hiện có.