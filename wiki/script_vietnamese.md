# [Hệ điều hành] C Shell (csh) script: Ghi lại phiên làm việc

## Overview
Lệnh `script` trong C Shell (csh) được sử dụng để ghi lại tất cả các hoạt động của người dùng trong một phiên làm việc. Nó tạo ra một tệp tin chứa tất cả các lệnh đã nhập và đầu ra của chúng, giúp người dùng có thể xem lại hoặc chia sẻ phiên làm việc của mình sau này.

## Usage
Cú pháp cơ bản của lệnh `script` như sau:

```csh
script [options] [arguments]
```

## Common Options
- `-a`: Thêm đầu ra vào tệp đã tồn tại thay vì ghi đè.
- `-f`: Hiển thị đầu ra ngay lập tức, không chờ đến khi phiên làm việc kết thúc.
- `-q`: Chạy lệnh mà không hiển thị thông báo bắt đầu và kết thúc.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `script`:

1. Ghi lại phiên làm việc vào tệp `session.log`:
   ```csh
   script session.log
   ```

2. Ghi thêm vào tệp đã tồn tại:
   ```csh
   script -a session.log
   ```

3. Ghi lại phiên làm việc và hiển thị đầu ra ngay lập tức:
   ```csh
   script -f session.log
   ```

4. Chạy lệnh mà không hiển thị thông báo:
   ```csh
   script -q session.log
   ```

## Tips
- Hãy nhớ kiểm tra kích thước của tệp tin ghi lại, vì nó có thể trở nên lớn nếu phiên làm việc kéo dài.
- Sử dụng tùy chọn `-a` nếu bạn muốn ghi lại nhiều phiên vào cùng một tệp mà không mất dữ liệu cũ.
- Để dừng ghi lại, chỉ cần gõ lệnh `exit` hoặc nhấn `Ctrl+D`.