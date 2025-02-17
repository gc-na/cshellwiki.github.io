# [Linux] Bash stat Cách sử dụng: Lấy thông tin về tệp tin

## Tổng quan
Lệnh `stat` được sử dụng để hiển thị thông tin chi tiết về một tệp tin hoặc thư mục trong hệ thống. Thông tin này bao gồm kích thước, thời gian sửa đổi, quyền truy cập và nhiều thông tin khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `stat` như sau:

```bash
stat [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-c`: Tùy chỉnh định dạng đầu ra.
- `--format`: Cung cấp định dạng cho thông tin đầu ra.
- `-f`: Hiển thị thông tin về hệ thống tệp.
- `--help`: Hiển thị trợ giúp sử dụng lệnh.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `stat`:

1. Hiển thị thông tin chi tiết về một tệp tin:

```bash
stat ten_tap_tin.txt
```

2. Hiển thị thông tin về một thư mục:

```bash
stat /duong_dan/thu_muc
```

3. Sử dụng tùy chọn `-c` để định dạng đầu ra:

```bash
stat -c '%n: %s bytes' ten_tap_tin.txt
```

4. Hiển thị thông tin về hệ thống tệp:

```bash
stat -f /
```

## Mẹo
- Sử dụng tùy chọn `--format` để tùy chỉnh thông tin bạn muốn xem, giúp bạn dễ dàng lấy thông tin cần thiết.
- Kết hợp lệnh `stat` với các lệnh khác như `grep` để lọc thông tin theo nhu cầu.
- Thường xuyên kiểm tra quyền truy cập của tệp tin để đảm bảo an toàn cho dữ liệu của bạn.