# [Linux] Bash renice: Thay đổi độ ưu tiên của tiến trình

## Overview
Lệnh `renice` được sử dụng để thay đổi độ ưu tiên của một hoặc nhiều tiến trình đang chạy trên hệ thống. Độ ưu tiên này ảnh hưởng đến cách mà hệ điều hành phân bổ tài nguyên CPU cho các tiến trình.

## Usage
Cú pháp cơ bản của lệnh `renice` như sau:

```bash
renice [options] [arguments]
```

## Common Options
- `-n, --priority <value>`: Xác định độ ưu tiên mới cho tiến trình. Giá trị có thể từ -20 (ưu tiên cao nhất) đến 19 (ưu tiên thấp nhất).
- `-p, --pid <pid>`: Chỉ định ID tiến trình (PID) mà bạn muốn thay đổi độ ưu tiên.
- `-g, --pgroup <pgid>`: Chỉ định nhóm tiến trình mà bạn muốn thay đổi độ ưu tiên.
- `-u, --user <username>`: Chỉ định người dùng mà bạn muốn thay đổi độ ưu tiên cho tất cả các tiến trình của họ.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `renice`:

1. Thay đổi độ ưu tiên của một tiến trình cụ thể:
   ```bash
   renice -n 10 -p 1234
   ```
   (Thay đổi độ ưu tiên của tiến trình có PID 1234 thành 10.)

2. Thay đổi độ ưu tiên cho tất cả các tiến trình của một người dùng:
   ```bash
   renice -n 5 -u username
   ```
   (Thay đổi độ ưu tiên của tất cả các tiến trình của người dùng `username` thành 5.)

3. Thay đổi độ ưu tiên cho một nhóm tiến trình:
   ```bash
   renice -n -5 -g 5678
   ```
   (Thay đổi độ ưu tiên của tất cả các tiến trình trong nhóm có PGID 5678 thành -5.)

## Tips
- Hãy cẩn thận khi thay đổi độ ưu tiên của các tiến trình quan trọng, vì điều này có thể ảnh hưởng đến hiệu suất hệ thống.
- Sử dụng quyền root hoặc sudo nếu bạn cần thay đổi độ ưu tiên cho các tiến trình của người dùng khác.
- Kiểm tra độ ưu tiên hiện tại của các tiến trình bằng lệnh `ps` để quyết định xem có cần thay đổi hay không.