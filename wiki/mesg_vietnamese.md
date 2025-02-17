# [Linux] Bash mesg Cách sử dụng: Quản lý quyền nhận tin nhắn

## Overview
Lệnh `mesg` trong Bash được sử dụng để quản lý quyền nhận tin nhắn từ người dùng khác trong một phiên làm việc. Khi bạn cho phép nhận tin nhắn, người khác có thể gửi tin nhắn cho bạn qua lệnh `write`. Ngược lại, nếu bạn từ chối, bạn sẽ không nhận được tin nhắn từ người khác.

## Usage
Cú pháp cơ bản của lệnh `mesg` như sau:
```
mesg [options] [arguments]
```

## Common Options
- `y`: Cho phép nhận tin nhắn từ người khác.
- `n`: Từ chối nhận tin nhắn từ người khác.
- `--help`: Hiển thị thông tin trợ giúp về lệnh `mesg`.
- `--version`: Hiển thị phiên bản của lệnh `mesg`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mesg`:

1. **Cho phép nhận tin nhắn:**
   ```bash
   mesg y
   ```

2. **Từ chối nhận tin nhắn:**
   ```bash
   mesg n
   ```

3. **Kiểm tra trạng thái hiện tại của quyền nhận tin nhắn:**
   ```bash
   mesg
   ```

## Tips
- Hãy chắc chắn rằng bạn chỉ cho phép nhận tin nhắn từ những người mà bạn tin tưởng để tránh bị làm phiền.
- Nếu bạn đang làm việc trong một môi trường công cộng, hãy cân nhắc việc từ chối nhận tin nhắn để giữ sự riêng tư.
- Bạn có thể kiểm tra trạng thái quyền nhận tin nhắn của mình bất cứ lúc nào bằng cách sử dụng lệnh `mesg` mà không có tham số.