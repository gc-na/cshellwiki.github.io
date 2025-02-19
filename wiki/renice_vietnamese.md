# [Hệ điều hành] C Shell (csh) renice: Thay đổi ưu tiên của tiến trình

## Overview
Lệnh `renice` trong C Shell (csh) được sử dụng để thay đổi mức độ ưu tiên của một hoặc nhiều tiến trình đang chạy. Điều này có thể hữu ích khi bạn muốn điều chỉnh tài nguyên hệ thống mà một tiến trình cụ thể sử dụng.

## Usage
Cú pháp cơ bản của lệnh `renice` như sau:
```csh
renice [options] [arguments]
```

## Common Options
- `-n`: Chỉ định mức độ ưu tiên mới cho tiến trình.
- `-p`: Chỉ định ID của tiến trình mà bạn muốn thay đổi mức độ ưu tiên.
- `-g`: Thay đổi mức độ ưu tiên cho một nhóm tiến trình.
- `-u`: Thay đổi mức độ ưu tiên cho tất cả tiến trình của một người dùng cụ thể.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `renice`:

1. Thay đổi mức độ ưu tiên của một tiến trình cụ thể:
   ```csh
   renice -n 10 -p 1234
   ```

2. Thay đổi mức độ ưu tiên cho tất cả tiến trình của một người dùng:
   ```csh
   renice -n 5 -u username
   ```

3. Thay đổi mức độ ưu tiên cho một nhóm tiến trình:
   ```csh
   renice -n 15 -g groupname
   ```

4. Kiểm tra mức độ ưu tiên của tiến trình:
   ```csh
   ps -o pid,ni,comm
   ```

## Tips
- Hãy cẩn thận khi thay đổi mức độ ưu tiên của tiến trình, vì việc đặt mức độ ưu tiên quá thấp có thể làm cho tiến trình không hoạt động hiệu quả.
- Sử dụng lệnh `ps` để theo dõi mức độ ưu tiên của các tiến trình trước và sau khi sử dụng `renice`.
- Chỉ thay đổi mức độ ưu tiên cho các tiến trình mà bạn có quyền truy cập, để tránh gặp phải lỗi quyền.