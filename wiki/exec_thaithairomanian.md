# [Linux] Bash exec sử dụng: Thực thi lệnh trong shell

## Overview
Lệnh `exec` trong Bash được sử dụng để thay thế shell hiện tại bằng một lệnh khác. Khi bạn sử dụng `exec`, lệnh mới sẽ chạy trong cùng một phiên làm việc, và shell hiện tại sẽ không còn tồn tại sau khi lệnh đó hoàn thành.

## Usage
Cú pháp cơ bản của lệnh `exec` như sau:
```bash
exec [options] [arguments]
```

## Common Options
- `-a` : Chỉ định tên khác cho lệnh được thực thi.
- `-l` : Thực thi lệnh như một shell đăng nhập.
- `-c` : Chạy lệnh trong một môi trường mới.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `exec`:

1. Thay thế shell hiện tại bằng một lệnh mới:
   ```bash
   exec ls -l
   ```

2. Chạy một lệnh với tên khác:
   ```bash
   exec -a my_custom_name /path/to/command
   ```

3. Thực thi một shell đăng nhập mới:
   ```bash
   exec -l bash
   ```

4. Chạy một lệnh trong một môi trường mới:
   ```bash
   exec -c env VAR=value command
   ```

## Tips
- Sử dụng `exec` khi bạn muốn thay thế shell hiện tại mà không cần mở một phiên shell mới.
- Hãy cẩn thận khi sử dụng `exec`, vì sau khi lệnh được thực thi, bạn sẽ không quay lại shell trước đó.
- Kiểm tra các lệnh bạn muốn thực thi với `exec` để đảm bảo chúng hoạt động như mong đợi trong môi trường hiện tại.