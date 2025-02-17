# [Linux] Bash nice cách sử dụng: Thay đổi ưu tiên của tiến trình

## Overview
Lệnh `nice` trong Bash được sử dụng để thay đổi mức độ ưu tiên của một tiến trình khi nó chạy. Mức độ ưu tiên này ảnh hưởng đến cách mà hệ điều hành phân bổ tài nguyên cho tiến trình, giúp cho người dùng có thể kiểm soát hiệu suất của các ứng dụng đang chạy.

## Usage
Cú pháp cơ bản của lệnh `nice` như sau:
```bash
nice [options] [arguments]
```

## Common Options
- `-n, --adjustment=N`: Điều chỉnh mức độ ưu tiên. Giá trị N có thể là số dương (giảm ưu tiên) hoặc số âm (tăng ưu tiên).
- `-h, --help`: Hiển thị thông tin trợ giúp về lệnh nice.
- `-v, --version`: Hiển thị phiên bản của lệnh nice.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `nice`:

1. **Chạy một tiến trình với mức độ ưu tiên thấp hơn**:
   ```bash
   nice -n 10 ./my_script.sh
   ```
   Lệnh này sẽ chạy `my_script.sh` với mức độ ưu tiên giảm đi 10.

2. **Chạy một tiến trình với mức độ ưu tiên cao hơn**:
   ```bash
   nice -n -5 ./my_heavy_process
   ```
   Lệnh này sẽ chạy `my_heavy_process` với mức độ ưu tiên tăng lên 5.

3. **Kiểm tra mức độ ưu tiên của một tiến trình**:
   ```bash
   ps -o pid,ni,cmd
   ```
   Lệnh này sẽ hiển thị PID, mức độ ưu tiên (nice value) và tên của các tiến trình đang chạy.

## Tips
- Sử dụng `nice` khi bạn muốn chạy các tiến trình không quan trọng mà không làm ảnh hưởng đến các tiến trình khác đang chạy trên hệ thống.
- Kiểm tra mức độ ưu tiên của các tiến trình hiện tại bằng lệnh `ps` để có quyết định tốt hơn về việc điều chỉnh ưu tiên.
- Hãy cẩn thận khi tăng mức độ ưu tiên cho các tiến trình quan trọng, vì điều này có thể làm chậm các tiến trình khác.