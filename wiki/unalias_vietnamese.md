# [Linux] Bash unalias: Xóa alias trong Bash

## Tổng quan
Lệnh `unalias` được sử dụng để xóa một hoặc nhiều alias đã được định nghĩa trong shell Bash. Alias là những tên gọi tắt cho các lệnh dài hoặc phức tạp, giúp người dùng tiết kiệm thời gian khi gõ lệnh.

## Cú pháp
Cú pháp cơ bản của lệnh `unalias` như sau:

```bash
unalias [tùy chọn] [alias]
```

## Các tùy chọn phổ biến
- `-a`: Xóa tất cả các alias đã được định nghĩa.
- `-p`: Hiển thị danh sách các alias hiện có mà không xóa chúng.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `unalias`:

1. **Xóa một alias cụ thể**:
   Giả sử bạn đã tạo một alias cho lệnh `ls` như sau:
   ```bash
   alias ls='ls --color=auto'
   ```
   Để xóa alias này, bạn sử dụng:
   ```bash
   unalias ls
   ```

2. **Xóa tất cả các alias**:
   Nếu bạn muốn xóa tất cả các alias đã định nghĩa, bạn có thể sử dụng:
   ```bash
   unalias -a
   ```

3. **Hiển thị danh sách các alias hiện có**:
   Để xem danh sách các alias mà bạn đã tạo, bạn có thể sử dụng:
   ```bash
   unalias -p
   ```

## Mẹo
- Hãy cẩn thận khi sử dụng `unalias -a`, vì lệnh này sẽ xóa tất cả alias mà bạn đã tạo, có thể làm mất đi những alias hữu ích.
- Nếu bạn chỉ muốn tạm thời xóa một alias, hãy xem xét việc định nghĩa lại alias đó với một tên khác thay vì xóa.
- Để tránh mất thời gian, hãy kiểm tra danh sách alias hiện có trước khi quyết định xóa chúng bằng cách sử dụng lệnh `alias`.