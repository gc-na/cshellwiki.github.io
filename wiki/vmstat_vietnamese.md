# [Linux] Bash vmstat Cách sử dụng: Theo dõi hiệu suất hệ thống

## Overview
Lệnh `vmstat` (Virtual Memory Statistics) được sử dụng để báo cáo thông tin về hiệu suất hệ thống, bao gồm bộ nhớ ảo, CPU, và các hoạt động I/O. Nó giúp người dùng theo dõi tình trạng hoạt động của hệ thống và phát hiện các vấn đề tiềm ẩn.

## Usage
Cú pháp cơ bản của lệnh `vmstat` như sau:

```bash
vmstat [options] [interval] [count]
```

## Common Options
- `-a`: Hiển thị thông tin về bộ nhớ đã sử dụng và bộ nhớ có thể sử dụng.
- `-m`: Hiển thị thông tin về bộ nhớ phân bổ cho các đối tượng.
- `-s`: Hiển thị thống kê bộ nhớ chi tiết.
- `-d`: Hiển thị thông tin về đĩa.
- `interval`: Thời gian giữa các lần báo cáo (tính bằng giây).
- `count`: Số lần báo cáo.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `vmstat`:

1. **Báo cáo hiệu suất hệ thống mỗi 2 giây**:
   ```bash
   vmstat 2
   ```

2. **Báo cáo thông tin bộ nhớ chi tiết**:
   ```bash
   vmstat -s
   ```

3. **Theo dõi thông tin về đĩa**:
   ```bash
   vmstat -d
   ```

4. **Báo cáo thông tin bộ nhớ ảo với 5 lần mỗi 1 giây**:
   ```bash
   vmstat 1 5
   ```

## Tips
- Sử dụng `vmstat` cùng với các lệnh khác như `top` hoặc `iostat` để có cái nhìn tổng quan hơn về hiệu suất hệ thống.
- Theo dõi thường xuyên để phát hiện các vấn đề về hiệu suất trước khi chúng trở thành nghiêm trọng.
- Lưu kết quả vào một tệp tin để phân tích sau này bằng cách sử dụng `>`:
  ```bash
  vmstat 2 > vmstat_output.txt
  ```