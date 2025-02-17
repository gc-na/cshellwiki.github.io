# [Linux] Bash diff cách sử dụng: So sánh sự khác biệt giữa các tệp

## Overview
Lệnh `diff` trong Bash được sử dụng để so sánh nội dung của hai tệp hoặc thư mục và hiển thị sự khác biệt giữa chúng. Lệnh này rất hữu ích trong việc kiểm tra các thay đổi trong mã nguồn hoặc tài liệu.

## Usage
Cú pháp cơ bản của lệnh `diff` như sau:

```bash
diff [options] [arguments]
```

## Common Options
- `-u`: Hiển thị sự khác biệt theo định dạng "unified", giúp dễ đọc hơn.
- `-c`: Hiển thị sự khác biệt theo định dạng "context", bao gồm một số dòng ngữ cảnh.
- `-i`: Bỏ qua sự khác biệt về chữ hoa và chữ thường.
- `-w`: Bỏ qua sự khác biệt về khoảng trắng.
- `-r`: So sánh các thư mục một cách đệ quy.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `diff`:

### So sánh hai tệp
```bash
diff file1.txt file2.txt
```

### Hiển thị sự khác biệt theo định dạng unified
```bash
diff -u file1.txt file2.txt
```

### So sánh hai thư mục
```bash
diff -r dir1/ dir2/
```

### Bỏ qua khoảng trắng
```bash
diff -w file1.txt file2.txt
```

## Tips
- Sử dụng tùy chọn `-u` để có cái nhìn rõ ràng hơn về sự khác biệt giữa các tệp.
- Khi làm việc với mã nguồn, hãy thường xuyên sử dụng `diff` để theo dõi các thay đổi.
- Kết hợp `diff` với các công cụ khác như `patch` để áp dụng các thay đổi một cách dễ dàng.