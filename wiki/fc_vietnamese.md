# [Linux] Bash fc <Sử dụng lệnh fc>: Quản lý lịch sử lệnh

## Overview
Lệnh `fc` trong Bash cho phép người dùng xem và chỉnh sửa các lệnh đã được thực hiện trước đó trong phiên làm việc của họ. Nó giúp người dùng dễ dàng truy cập và sửa đổi các lệnh mà họ đã nhập, giúp tiết kiệm thời gian và công sức.

## Usage
Cú pháp cơ bản của lệnh `fc` như sau:
```bash
fc [options] [arguments]
```

## Common Options
- `-l`: Liệt kê các lệnh trong lịch sử.
- `-r`: Đảo ngược thứ tự các lệnh khi liệt kê.
- `-s`: Chạy lệnh mà không hiển thị nó trong trình soạn thảo.
- `-n`: Không hiển thị số thứ tự của lệnh khi liệt kê.

## Common Examples
1. **Liệt kê các lệnh trong lịch sử**:
   ```bash
   fc -l
   ```

2. **Liệt kê các lệnh trong lịch sử với số thứ tự**:
   ```bash
   fc -l -n
   ```

3. **Chạy lệnh cuối cùng mà không chỉnh sửa**:
   ```bash
   fc -s
   ```

4. **Chỉnh sửa lệnh thứ 5 trong lịch sử**:
   ```bash
   fc 5
   ```

5. **Liệt kê các lệnh theo thứ tự đảo ngược**:
   ```bash
   fc -r -l
   ```

## Tips
- Sử dụng `fc` để nhanh chóng sửa đổi các lệnh phức tạp mà bạn đã nhập trước đó.
- Kết hợp `fc` với các trình soạn thảo như `nano` hoặc `vim` để có trải nghiệm chỉnh sửa tốt hơn.
- Hãy nhớ rằng `fc` chỉ hoạt động trong phiên Bash hiện tại, vì vậy nếu bạn khởi động lại terminal, lịch sử sẽ không còn.