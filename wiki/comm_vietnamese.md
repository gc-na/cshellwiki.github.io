# [Linux] Bash comm lệnh: So sánh hai tệp

## Overview
Lệnh `comm` trong Bash được sử dụng để so sánh hai tệp đã được sắp xếp và hiển thị các dòng chung, dòng chỉ có trong tệp đầu tiên và dòng chỉ có trong tệp thứ hai. Đây là một công cụ hữu ích để phân tích sự khác biệt giữa hai tệp văn bản.

## Usage
Cú pháp cơ bản của lệnh `comm` như sau:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Ẩn các dòng chỉ có trong tệp đầu tiên.
- `-2`: Ẩn các dòng chỉ có trong tệp thứ hai.
- `-3`: Ẩn các dòng chung giữa hai tệp.
- `-i`: Bỏ qua sự khác biệt về chữ hoa chữ thường khi so sánh.
- `-u`: Hiển thị các dòng duy nhất từ cả hai tệp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `comm`:

### Ví dụ 1: So sánh hai tệp
Giả sử bạn có hai tệp `file1.txt` và `file2.txt`, bạn có thể so sánh chúng như sau:

```bash
comm file1.txt file2.txt
```

### Ví dụ 2: Chỉ hiển thị các dòng chung
Nếu bạn chỉ muốn xem các dòng chung giữa hai tệp, bạn có thể sử dụng tùy chọn `-1` và `-2`:

```bash
comm -12 file1.txt file2.txt
```

### Ví dụ 3: Hiển thị các dòng chỉ có trong tệp thứ hai
Để chỉ hiển thị các dòng chỉ có trong `file2.txt`, bạn có thể sử dụng tùy chọn `-1`:

```bash
comm -13 file1.txt file2.txt
```

### Ví dụ 4: So sánh không phân biệt chữ hoa chữ thường
Nếu bạn muốn so sánh mà không phân biệt chữ hoa chữ thường, hãy sử dụng tùy chọn `-i`:

```bash
comm -i file1.txt file2.txt
```

## Tips
- Đảm bảo rằng các tệp bạn muốn so sánh đã được sắp xếp. Bạn có thể sử dụng lệnh `sort` để sắp xếp tệp trước khi sử dụng `comm`.
- Sử dụng các tùy chọn để điều chỉnh kết quả hiển thị theo nhu cầu của bạn.
- Kết hợp lệnh `comm` với các lệnh khác trong Bash để tự động hóa quy trình phân tích tệp.