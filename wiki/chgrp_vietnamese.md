# [Linux] Bash chgrp Cách sử dụng: Thay đổi nhóm sở hữu của file

## Overview
Lệnh `chgrp` trong Bash được sử dụng để thay đổi nhóm sở hữu của một hoặc nhiều file hoặc thư mục. Điều này cho phép người dùng quản lý quyền truy cập và quyền sở hữu của các file trong hệ thống.

## Usage
Cú pháp cơ bản của lệnh `chgrp` như sau:
```
chgrp [options] [arguments]
```

## Common Options
- `-R`: Thay đổi nhóm sở hữu cho tất cả các file và thư mục con trong thư mục được chỉ định.
- `-v`: Hiển thị thông tin chi tiết về các thay đổi đã thực hiện.
- `-c`: Hiển thị chỉ các thay đổi mà lệnh đã thực hiện.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `chgrp`:

1. Thay đổi nhóm sở hữu của một file đơn:
   ```bash
   chgrp group_name filename.txt
   ```

2. Thay đổi nhóm sở hữu của nhiều file:
   ```bash
   chgrp group_name file1.txt file2.txt file3.txt
   ```

3. Thay đổi nhóm sở hữu cho một thư mục và tất cả các file bên trong:
   ```bash
   chgrp -R group_name /path/to/directory
   ```

4. Hiển thị thông tin chi tiết về các thay đổi:
   ```bash
   chgrp -v group_name filename.txt
   ```

## Tips
- Hãy chắc chắn rằng bạn có quyền để thay đổi nhóm sở hữu của file hoặc thư mục.
- Sử dụng tùy chọn `-R` cẩn thận, vì nó sẽ thay đổi nhóm cho tất cả các file và thư mục con.
- Kiểm tra nhóm hiện tại của file bằng lệnh `ls -l` trước khi thực hiện thay đổi.