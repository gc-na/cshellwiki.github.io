# [Linux] Bash wall cách sử dụng: Gửi thông báo đến tất cả người dùng

## Overview
Lệnh `wall` (viết tắt của "write all") được sử dụng để gửi thông báo đến tất cả người dùng đang đăng nhập trên hệ thống. Thông báo này sẽ hiển thị trên màn hình của họ, giúp người quản trị hệ thống truyền đạt thông tin quan trọng một cách nhanh chóng.

## Usage
Cú pháp cơ bản của lệnh `wall` như sau:

```bash
wall [options] [arguments]
```

## Common Options
- `-n`: Không hiển thị tên người gửi trong thông báo.
- `-s`: Gửi thông báo mà không có định dạng, chỉ gửi nội dung thuần túy.
- `-f`: Gửi thông báo từ một tệp tin cụ thể.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `wall`:

1. Gửi một thông báo đơn giản đến tất cả người dùng:
   ```bash
   wall "Hệ thống sẽ bảo trì vào lúc 10 giờ tối hôm nay."
   ```

2. Gửi thông báo từ một tệp tin:
   ```bash
   wall -f thongbao.txt
   ```

3. Gửi thông báo mà không hiển thị tên người gửi:
   ```bash
   wall -n "Xin lưu ý: Hệ thống sẽ khởi động lại trong 5 phút."
   ```

4. Gửi thông báo với định dạng thuần túy:
   ```bash
   wall -s "Cảnh báo: Mất điện sắp xảy ra!"
   ```

## Tips
- Trước khi gửi thông báo, hãy chắc chắn rằng nội dung thông báo rõ ràng và dễ hiểu để người nhận có thể nắm bắt thông tin nhanh chóng.
- Sử dụng lệnh `wall` trong các tình huống khẩn cấp hoặc khi cần thông báo cho nhiều người dùng cùng một lúc.
- Kiểm tra xem có người dùng nào đang hoạt động trên hệ thống trước khi gửi thông báo để đảm bảo rằng thông điệp của bạn sẽ được nhận.