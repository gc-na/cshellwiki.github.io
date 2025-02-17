# [Linux] Bash pr: [in ấn tài liệu]

## Overview
Lệnh `pr` trong Bash được sử dụng để định dạng và in nội dung của các tệp tin văn bản. Nó giúp người dùng tạo ra các trang in có định dạng đẹp mắt, dễ đọc hơn bằng cách chia nội dung thành các cột và thêm tiêu đề.

## Usage
Cú pháp cơ bản của lệnh `pr` như sau:
```bash
pr [options] [arguments]
```

## Common Options
- `-h, --header=HEADER`: Thêm tiêu đề cho trang in.
- `-l, --length=NUMBER`: Đặt chiều dài trang in (số dòng trên mỗi trang).
- `-n, --number`: Đánh số dòng trong tài liệu.
- `-t, --omit-header`: Bỏ qua tiêu đề trang.
- `-s, --separator=CHAR`: Đặt ký tự phân cách giữa các cột.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `pr`:

1. **In một tệp tin với tiêu đề**:
   ```bash
   pr -h "Tiêu đề Tài liệu" file.txt
   ```

2. **In tệp tin với 2 cột**:
   ```bash
   pr -2 file.txt
   ```

3. **In tệp tin với số dòng**:
   ```bash
   pr -n file.txt
   ```

4. **In tệp tin với chiều dài trang là 50 dòng**:
   ```bash
   pr -l 50 file.txt
   ```

5. **In tệp tin mà không có tiêu đề**:
   ```bash
   pr -t file.txt
   ```

## Tips
- Sử dụng tùy chọn `-h` để thêm tiêu đề giúp tài liệu của bạn trở nên chuyên nghiệp hơn.
- Kết hợp các tùy chọn như `-2` và `-n` để tạo ra một tài liệu dễ đọc và có tổ chức.
- Kiểm tra nội dung trước khi in để đảm bảo rằng định dạng phù hợp với yêu cầu của bạn.