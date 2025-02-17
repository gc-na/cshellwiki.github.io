# [Linux] Bash vipw Cách sử dụng: Chỉnh sửa tệp passwd an toàn

## Overview
Lệnh `vipw` được sử dụng để chỉnh sửa tệp passwd một cách an toàn. Nó đảm bảo rằng chỉ một phiên bản của tệp passwd được mở trong quá trình chỉnh sửa, giúp ngăn chặn các lỗi có thể xảy ra do nhiều người dùng chỉnh sửa cùng một lúc.

## Usage
Cú pháp cơ bản của lệnh `vipw` như sau:
```
vipw [options]
```

## Common Options
- `-s`: Sử dụng tùy chọn này để chỉnh sửa tệp shadow thay vì tệp passwd.
- `-m`: Tùy chọn này cho phép bạn chỉnh sửa tệp nhóm (group file) thay vì tệp passwd.

## Common Examples
- Mở tệp passwd để chỉnh sửa:
  ```bash
  vipw
  ```

- Mở tệp shadow để chỉnh sửa:
  ```bash
  vipw -s
  ```

- Mở tệp nhóm để chỉnh sửa:
  ```bash
  vipw -m
  ```

## Tips
- Luôn sao lưu tệp passwd trước khi thực hiện bất kỳ thay đổi nào để tránh mất mát dữ liệu.
- Kiểm tra kỹ các thay đổi trước khi lưu để đảm bảo không có lỗi cú pháp.
- Sử dụng `vipw` thay vì chỉnh sửa trực tiếp tệp passwd bằng các trình soạn thảo khác để bảo vệ tính toàn vẹn của tệp.