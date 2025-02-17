# [Linux] Bash xz Sử dụng: Nén và giải nén tệp tin

## Overview
Lệnh `xz` được sử dụng để nén và giải nén các tệp tin, giúp tiết kiệm không gian lưu trữ. Nó sử dụng thuật toán nén LZMA, mang lại hiệu suất nén cao hơn so với nhiều công cụ nén khác.

## Usage
Cú pháp cơ bản của lệnh `xz` như sau:
```
xz [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: Giải nén tệp tin.
- `-k`, `--keep`: Giữ lại tệp tin gốc sau khi nén.
- `-f`, `--force`: Buộc ghi đè tệp tin đã tồn tại.
- `-z`, `--compress`: Nén tệp tin (mặc định).
- `-9`: Sử dụng mức nén cao nhất.

## Common Examples
- Nén một tệp tin:
  ```bash
  xz file.txt
  ```
- Giải nén một tệp tin đã nén:
  ```bash
  xz -d file.txt.xz
  ```
- Nén tệp tin và giữ lại tệp gốc:
  ```bash
  xz -k file.txt
  ```
- Giải nén tất cả các tệp tin `.xz` trong thư mục hiện tại:
  ```bash
  xz -d *.xz
  ```

## Tips
- Sử dụng tùy chọn `-9` để đạt được mức nén tối đa, nhưng hãy lưu ý rằng điều này có thể làm tăng thời gian nén.
- Kiểm tra dung lượng tệp trước và sau khi nén để đánh giá hiệu quả.
- Kết hợp `xz` với `tar` để nén nhiều tệp tin thành một tệp duy nhất, ví dụ:
  ```bash
  tar -cJf archive.tar.xz folder/
  ```