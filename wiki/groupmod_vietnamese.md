# [Linux] Bash groupmod Cách sử dụng: Thay đổi thông tin của nhóm

## Tổng quan
Lệnh `groupmod` được sử dụng để thay đổi thông tin của một nhóm người dùng trong hệ thống Linux. Nó cho phép bạn sửa đổi tên nhóm, ID nhóm và các thuộc tính khác của nhóm.

## Cách sử dụng
Cú pháp cơ bản của lệnh `groupmod` như sau:

```bash
groupmod [options] [arguments]
```

## Các tùy chọn phổ biến
- `-n, --new-name NEW_GROUP`: Đổi tên nhóm thành NEW_GROUP.
- `-g, --gid GID`: Thay đổi ID nhóm thành GID.
- `-o, --non-unique`: Cho phép sử dụng GID không duy nhất.

## Ví dụ thường gặp
1. **Đổi tên nhóm**:
   ```bash
   groupmod -n newgroup oldgroup
   ```

2. **Thay đổi ID nhóm**:
   ```bash
   groupmod -g 1001 mygroup
   ```

3. **Thay đổi tên nhóm và ID nhóm cùng lúc**:
   ```bash
   groupmod -n newgroup -g 1002 oldgroup
   ```

4. **Cho phép GID không duy nhất**:
   ```bash
   groupmod -o -g 1001 anothergroup
   ```

## Mẹo
- Trước khi thay đổi tên hoặc ID nhóm, hãy chắc chắn rằng không có người dùng nào đang sử dụng nhóm đó để tránh xung đột.
- Sử dụng lệnh `getent group` để kiểm tra thông tin nhóm trước và sau khi thực hiện thay đổi.
- Đảm bảo rằng bạn có quyền quản trị (root) để thực hiện các thay đổi này.