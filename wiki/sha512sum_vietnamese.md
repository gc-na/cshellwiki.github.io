# [Hệ điều hành] C Shell (csh) sha512sum: Tính toán và xác minh mã băm SHA-512

## Overview
Lệnh `sha512sum` được sử dụng để tính toán và xác minh mã băm SHA-512 cho các tệp. Mã băm SHA-512 là một chuỗi ký tự đại diện cho nội dung của tệp, giúp người dùng kiểm tra tính toàn vẹn của tệp đó.

## Usage
Cú pháp cơ bản của lệnh `sha512sum` như sau:

```csh
sha512sum [options] [arguments]
```

## Common Options
- `-b`: Chỉ định rằng tệp đầu vào là nhị phân.
- `-c`: Kiểm tra mã băm SHA-512 từ một tệp danh sách.
- `-h`: Hiển thị thông tin trợ giúp về lệnh.
- `--tag`: Thêm tag vào đầu ra.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sha512sum`:

1. Tính toán mã băm SHA-512 cho một tệp:
   ```csh
   sha512sum myfile.txt
   ```

2. Lưu mã băm vào một tệp:
   ```csh
   sha512sum myfile.txt > myfile.sha512
   ```

3. Kiểm tra mã băm từ một tệp danh sách:
   ```csh
   sha512sum -c myfile.sha512
   ```

4. Tính toán mã băm cho nhiều tệp cùng một lúc:
   ```csh
   sha512sum file1.txt file2.txt file3.txt
   ```

## Tips
- Luôn kiểm tra mã băm của tệp sau khi tải xuống để đảm bảo tính toàn vẹn.
- Sử dụng tùy chọn `-c` để tự động kiểm tra nhiều tệp băm từ một tệp danh sách.
- Lưu trữ mã băm ở nơi an toàn để có thể tham chiếu lại khi cần thiết.