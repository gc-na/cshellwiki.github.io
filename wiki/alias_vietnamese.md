# [Linux] Bash alias: Tạo bí danh cho lệnh

## Overview
Lệnh `alias` trong Bash cho phép người dùng tạo bí danh cho các lệnh dài hoặc phức tạp, giúp tiết kiệm thời gian và công sức khi gõ lệnh trong terminal. Bằng cách sử dụng alias, bạn có thể thay thế một lệnh dài bằng một từ khóa ngắn gọn hơn.

## Usage
Cú pháp cơ bản của lệnh alias như sau:
```bash
alias [tùy chọn] [bí danh]='[lệnh]'
```

## Common Options
- `-p`: Hiển thị tất cả các bí danh hiện có.
- `--help`: Hiển thị thông tin trợ giúp về lệnh alias.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh alias:

1. Tạo bí danh cho lệnh `ls -la`:
   ```bash
   alias ll='ls -la'
   ```

2. Tạo bí danh cho lệnh `git status`:
   ```bash
   alias gs='git status'
   ```

3. Tạo bí danh để cập nhật hệ thống (trên Ubuntu):
   ```bash
   alias update='sudo apt update && sudo apt upgrade'
   ```

4. Hiển thị tất cả các bí danh hiện có:
   ```bash
   alias -p
   ```

## Tips
- Để giữ các bí danh sau khi khởi động lại terminal, bạn có thể thêm chúng vào tệp cấu hình như `.bashrc` hoặc `.bash_profile`.
- Hãy chọn tên bí danh ngắn gọn nhưng dễ nhớ để dễ dàng sử dụng.
- Tránh tạo bí danh trùng với các lệnh hệ thống có sẵn để tránh nhầm lẫn.