# [Linux] Bash dig Cách sử dụng: Truy vấn thông tin DNS

## Tổng quan
Lệnh `dig` (Domain Information Groper) là một công cụ dòng lệnh được sử dụng để truy vấn thông tin DNS (Domain Name System). Nó cho phép người dùng lấy thông tin về tên miền, địa chỉ IP và các bản ghi DNS khác một cách chi tiết và rõ ràng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `dig` như sau:

```bash
dig [options] [arguments]
```

## Các tùy chọn phổ biến
- `@server`: Chỉ định máy chủ DNS để truy vấn.
- `-t type`: Chỉ định loại bản ghi DNS (ví dụ: A, AAAA, MX, TXT).
- `+short`: Hiển thị kết quả ngắn gọn, chỉ hiển thị thông tin quan trọng.
- `+trace`: Theo dõi quá trình truy vấn DNS từ máy chủ gốc.

## Ví dụ thường gặp
- Truy vấn địa chỉ IP của một tên miền:

```bash
dig example.com
```

- Truy vấn bản ghi MX (Mail Exchange) của một tên miền:

```bash
dig example.com -t MX
```

- Sử dụng máy chủ DNS cụ thể để truy vấn:

```bash
dig @8.8.8.8 example.com
```

- Hiển thị kết quả ngắn gọn:

```bash
dig example.com +short
```

- Theo dõi quá trình truy vấn DNS:

```bash
dig example.com +trace
```

## Mẹo
- Sử dụng tùy chọn `+short` để có được kết quả nhanh chóng và dễ hiểu, đặc biệt khi bạn chỉ cần thông tin cụ thể.
- Nếu bạn thường xuyên làm việc với nhiều tên miền, hãy tạo một tập tin shell script để tự động hóa các truy vấn `dig`.
- Kiểm tra các bản ghi DNS của một tên miền từ nhiều máy chủ DNS khác nhau để xác minh tính chính xác và độ tin cậy của thông tin.