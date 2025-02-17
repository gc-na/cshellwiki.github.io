# [Linux] Bash cmp cách sử dụng: So sánh nội dung của hai tệp

## Tổng quan
Lệnh `cmp` trong Bash được sử dụng để so sánh nội dung của hai tệp. Nếu hai tệp giống nhau, lệnh sẽ không xuất ra gì. Nếu có sự khác biệt, lệnh sẽ chỉ ra vị trí và loại khác biệt giữa chúng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `cmp` như sau:
```bash
cmp [tùy chọn] [tệp1] [tệp2]
```

## Tùy chọn phổ biến
- `-l`: Hiển thị các byte khác nhau và vị trí của chúng.
- `-s`: Chỉ kiểm tra xem hai tệp có khác nhau hay không, không xuất ra thông tin chi tiết.
- `-i`: Bỏ qua số byte đầu tiên khi so sánh.
- `-n`: Chỉ so sánh số byte nhất định từ đầu tệp.

## Ví dụ phổ biến
- So sánh hai tệp:
```bash
cmp file1.txt file2.txt
```

- So sánh và hiển thị các byte khác nhau:
```bash
cmp -l file1.txt file2.txt
```

- Kiểm tra sự khác biệt mà không xuất ra thông tin:
```bash
cmp -s file1.txt file2.txt
```

- So sánh chỉ 10 byte đầu tiên của hai tệp:
```bash
cmp -n 10 file1.txt file2.txt
```

## Mẹo
- Sử dụng tùy chọn `-s` để nhanh chóng kiểm tra xem hai tệp có giống nhau hay không mà không cần thông tin chi tiết.
- Khi làm việc với các tệp nhị phân, `cmp` là một công cụ hữu ích để phát hiện sự khác biệt mà không cần mở tệp.
- Kết hợp `cmp` với các lệnh khác như `find` để tự động so sánh nhiều tệp trong một thư mục.