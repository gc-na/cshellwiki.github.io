# [Linux] Bash mkswap: Tạo không gian hoán đổi cho hệ thống

## Overview
Lệnh `mkswap` được sử dụng để tạo một không gian hoán đổi (swap space) trên một thiết bị hoặc tệp tin. Không gian hoán đổi là một phần của bộ nhớ ảo, cho phép hệ thống sử dụng không gian trên đĩa cứng như một phần của bộ nhớ RAM, giúp cải thiện hiệu suất khi bộ nhớ vật lý bị đầy.

## Usage
Cú pháp cơ bản của lệnh `mkswap` như sau:

```bash
mkswap [options] [arguments]
```

## Common Options
- `-L, --label <label>`: Gán nhãn cho không gian hoán đổi.
- `-f, --force`: Bỏ qua các cảnh báo và ép buộc tạo không gian hoán đổi.
- `-p, --pagesize <size>`: Xác định kích thước trang cho không gian hoán đổi.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mkswap`:

1. **Tạo không gian hoán đổi từ một tệp tin**:
   ```bash
   sudo fallocate -l 1G /swapfile
   sudo mkswap /swapfile
   ```

2. **Tạo không gian hoán đổi từ một phân vùng**:
   ```bash
   sudo mkswap /dev/sdX1
   ```

3. **Tạo không gian hoán đổi với nhãn**:
   ```bash
   sudo mkswap -L my_swap /dev/sdX1
   ```

4. **Ép buộc tạo không gian hoán đổi**:
   ```bash
   sudo mkswap -f /dev/sdX1
   ```

## Tips
- Đảm bảo rằng tệp tin hoặc phân vùng bạn muốn sử dụng cho không gian hoán đổi đã được tạo và không chứa dữ liệu quan trọng.
- Sau khi tạo không gian hoán đổi, bạn cần kích hoạt nó bằng lệnh `swapon`.
- Kiểm tra trạng thái không gian hoán đổi bằng lệnh `swapon --show` để đảm bảo nó đã được kích hoạt thành công.