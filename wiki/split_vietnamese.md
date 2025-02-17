# [Linux] Bash split cách sử dụng: Chia tách tệp tin lớn thành các phần nhỏ

## Overview
Lệnh `split` trong Bash được sử dụng để chia tách một tệp tin lớn thành nhiều tệp tin nhỏ hơn. Điều này hữu ích khi bạn cần xử lý hoặc truyền tải dữ liệu mà không muốn làm việc với một tệp tin quá lớn.

## Usage
Cú pháp cơ bản của lệnh `split` như sau:

```bash
split [options] [arguments]
```

## Common Options
- `-l [number]`: Chia tệp tin thành các phần với số dòng cụ thể.
- `-b [size]`: Chia tệp tin thành các phần với kích thước cụ thể (ví dụ: 1k cho 1 kilobyte).
- `-d`: Sử dụng số để đánh số các tệp tin đầu ra.
- `--additional-suffix=[suffix]`: Thêm hậu tố vào tên tệp tin đầu ra.

## Common Examples
- Chia tệp tin thành các phần 100 dòng mỗi phần:

```bash
split -l 100 input.txt
```

- Chia tệp tin thành các phần 1MB mỗi phần:

```bash
split -b 1M input.txt
```

- Chia tệp tin và sử dụng số để đánh số các tệp tin đầu ra:

```bash
split -d -l 50 input.txt output_prefix_
```

- Chia tệp tin và thêm hậu tố `.txt` vào các tệp tin đầu ra:

```bash
split --additional-suffix=.txt -l 10 input.txt output_prefix_
```

## Tips
- Khi chia tách tệp tin lớn, hãy chắc chắn rằng bạn có đủ không gian lưu trữ cho các tệp tin đầu ra.
- Sử dụng tùy chọn `-d` để dễ dàng quản lý và xác định các tệp tin đầu ra.
- Kiểm tra kích thước và số lượng dòng của tệp tin đầu vào trước khi chia tách để có kế hoạch phù hợp.