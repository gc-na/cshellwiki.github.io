# [Hệ điều hành] C Shell (csh) cd: Di chuyển giữa các thư mục

## Overview
Lệnh `cd` (change directory) trong C Shell được sử dụng để thay đổi thư mục làm việc hiện tại. Khi bạn sử dụng lệnh này, bạn có thể di chuyển đến bất kỳ thư mục nào trên hệ thống tệp của bạn.

## Usage
Cú pháp cơ bản của lệnh `cd` như sau:
```
cd [tùy chọn] [đối số]
```

## Common Options
- `-`: Quay lại thư mục trước đó.
- `~`: Chuyển đến thư mục chính của người dùng hiện tại.
- `..`: Di chuyển lên một cấp thư mục.

## Common Examples
- Di chuyển đến thư mục chính của người dùng:
  ```csh
  cd ~
  ```

- Di chuyển đến thư mục cha:
  ```csh
  cd ..
  ```

- Di chuyển đến một thư mục cụ thể:
  ```csh
  cd /path/to/directory
  ```

- Quay lại thư mục trước đó:
  ```csh
  cd -
  ```

## Tips
- Sử dụng `cd ~` để nhanh chóng trở về thư mục chính của bạn.
- Bạn có thể sử dụng `cd ..` nhiều lần để di chuyển lên nhiều cấp thư mục.
- Để kiểm tra thư mục hiện tại, bạn có thể sử dụng lệnh `pwd` sau khi thay đổi thư mục.