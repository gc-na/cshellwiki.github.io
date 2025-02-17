# [Linux] Bash popd Cách sử dụng: Quay lại thư mục trước đó

## Overview
Lệnh `popd` trong Bash được sử dụng để quay lại thư mục trước đó trong ngăn xếp thư mục. Khi bạn di chuyển giữa các thư mục bằng lệnh `pushd`, `popd` sẽ giúp bạn trở về thư mục mà bạn đã lưu trước đó.

## Usage
Cú pháp cơ bản của lệnh `popd` như sau:

```bash
popd [options]
```

## Common Options
- `-n`: Không thay đổi thư mục hiện tại, chỉ xóa thư mục khỏi ngăn xếp.
- `+n`: Quay lại thư mục thứ n từ trên cùng của ngăn xếp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `popd`:

1. **Quay lại thư mục trước đó**:
   ```bash
   pushd /path/to/directory1
   pushd /path/to/directory2
   popd
   ```

2. **Quay lại thư mục thứ hai trong ngăn xếp**:
   ```bash
   pushd /path/to/directory1
   pushd /path/to/directory2
   pushd /path/to/directory3
   popd +1
   ```

3. **Sử dụng tùy chọn -n để không thay đổi thư mục hiện tại**:
   ```bash
   pushd /path/to/directory1
   pushd /path/to/directory2
   popd -n
   ```

## Tips
- Sử dụng `pushd` và `popd` để quản lý thư mục hiệu quả hơn khi làm việc với nhiều thư mục cùng lúc.
- Kiểm tra ngăn xếp thư mục hiện tại bằng lệnh `dirs` để biết vị trí của các thư mục đã được lưu.
- Kết hợp `popd` với các lệnh khác để tự động hóa quy trình làm việc của bạn.