# [Linux] Bash sha256sum Cách sử dụng: Tính toán và xác minh giá trị băm SHA-256

## Overview
Lệnh `sha256sum` được sử dụng để tính toán và xác minh giá trị băm SHA-256 của một tệp tin. Giá trị băm này có thể được sử dụng để kiểm tra tính toàn vẹn của dữ liệu, đảm bảo rằng tệp không bị thay đổi hoặc hỏng hóc.

## Usage
Cú pháp cơ bản của lệnh `sha256sum` như sau:
```bash
sha256sum [options] [arguments]
```

## Common Options
- `-b`, `--binary`: Xử lý tệp tin nhị phân.
- `-c`, `--check`: Kiểm tra các tệp tin băm đã được lưu trữ.
- `-t`, `--text`: Xử lý tệp tin văn bản (mặc định).
- `--quiet`: Không in ra thông tin bổ sung khi kiểm tra.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `sha256sum`:

1. **Tính toán giá trị băm của một tệp tin**:
   ```bash
   sha256sum example.txt
   ```

2. **Lưu giá trị băm vào một tệp tin**:
   ```bash
   sha256sum example.txt > example.sha256
   ```

3. **Kiểm tra giá trị băm từ một tệp tin đã lưu**:
   ```bash
   sha256sum -c example.sha256
   ```

4. **Tính toán giá trị băm cho nhiều tệp tin**:
   ```bash
   sha256sum file1.txt file2.txt
   ```

## Tips
- Luôn lưu giá trị băm của tệp tin quan trọng để có thể kiểm tra lại sau này.
- Sử dụng tùy chọn `-c` để kiểm tra tính toàn vẹn của tệp tin sau khi truyền tải hoặc sao chép.
- Đảm bảo rằng bạn đang sử dụng phiên bản mới nhất của `sha256sum` để có được các tính năng và sửa lỗi mới nhất.