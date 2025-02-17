# [Linux] Bash cd cách sử dụng: Chuyển đổi thư mục làm việc

## Tổng quan
Lệnh `cd` (change directory) trong Bash được sử dụng để thay đổi thư mục làm việc hiện tại của người dùng. Khi bạn muốn di chuyển giữa các thư mục trong hệ thống tệp, lệnh này là công cụ chính để thực hiện điều đó.

## Cách sử dụng
Cú pháp cơ bản của lệnh `cd` như sau:

```bash
cd [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `..` : Di chuyển lên một cấp thư mục.
- `-` : Quay lại thư mục trước đó.
- `~` : Di chuyển đến thư mục chính của người dùng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `cd`:

1. Di chuyển đến thư mục cha:
   ```bash
   cd ..
   ```

2. Quay lại thư mục trước đó:
   ```bash
   cd -
   ```

3. Di chuyển đến thư mục chính của người dùng:
   ```bash
   cd ~
   ```

4. Di chuyển đến một thư mục cụ thể:
   ```bash
   cd /path/to/directory
   ```

5. Di chuyển đến thư mục con:
   ```bash
   cd subdirectory
   ```

## Mẹo
- Sử dụng phím Tab để tự động hoàn thành tên thư mục, giúp tiết kiệm thời gian và giảm lỗi.
- Kiểm tra thư mục hiện tại bằng lệnh `pwd` trước khi sử dụng `cd` để đảm bảo bạn đang ở đúng vị trí.
- Nếu bạn thường xuyên làm việc với một thư mục cụ thể, hãy cân nhắc tạo một alias trong file cấu hình shell của bạn để truy cập nhanh hơn.