# [Linux] Bash rehash sử dụng: Cập nhật danh sách lệnh

## Overview
Lệnh `rehash` trong Bash được sử dụng để cập nhật danh sách các lệnh có sẵn trong shell. Khi bạn thêm hoặc xóa các chương trình trong thư mục chứa các lệnh, việc sử dụng `rehash` sẽ giúp shell nhận biết những thay đổi này mà không cần khởi động lại.

## Usage
Cú pháp cơ bản của lệnh `rehash` như sau:
```bash
rehash [options] [arguments]
```

## Common Options
- Không có tùy chọn đặc biệt nào cho lệnh `rehash`. Lệnh này chủ yếu được sử dụng mà không cần thêm tùy chọn.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `rehash`:

1. **Cập nhật danh sách lệnh sau khi cài đặt một chương trình mới:**
   ```bash
   rehash
   ```

2. **Sử dụng `rehash` sau khi xóa một lệnh:**
   ```bash
   rehash
   ```

3. **Khi bạn đã thêm một thư mục mới vào biến môi trường PATH:**
   ```bash
   export PATH=$PATH:/new/directory
   rehash
   ```

## Tips
- Sử dụng `rehash` sau khi cài đặt hoặc xóa các chương trình để đảm bảo rằng shell của bạn có danh sách lệnh chính xác.
- Nếu bạn đang làm việc trong một phiên Bash tương tác, hãy nhớ rằng `rehash` có thể giúp bạn tiết kiệm thời gian thay vì khởi động lại shell.
- Lệnh này thường không cần thiết trong các phiên Bash hiện đại, vì chúng tự động cập nhật danh sách lệnh. Tuy nhiên, trong một số trường hợp, việc sử dụng `rehash` vẫn có thể hữu ích.