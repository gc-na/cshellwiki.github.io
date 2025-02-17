# [Linux] Bash curl cách sử dụng: Gửi và nhận dữ liệu qua giao thức HTTP

## Tổng quan
Lệnh `curl` là một công cụ dòng lệnh mạnh mẽ cho phép người dùng gửi và nhận dữ liệu từ hoặc đến một máy chủ thông qua các giao thức như HTTP, HTTPS, FTP, và nhiều hơn nữa. Nó thường được sử dụng để kiểm tra API, tải xuống tệp, hoặc gửi dữ liệu đến máy chủ.

## Cách sử dụng
Cú pháp cơ bản của lệnh `curl` như sau:
```bash
curl [options] [arguments]
```

## Các tùy chọn phổ biến
- `-X`: Chỉ định phương thức HTTP (GET, POST, PUT, DELETE, v.v.).
- `-d`: Gửi dữ liệu trong yêu cầu POST.
- `-H`: Thêm tiêu đề HTTP vào yêu cầu.
- `-o`: Chỉ định tệp đầu ra để lưu dữ liệu nhận được.
- `-I`: Chỉ nhận tiêu đề của phản hồi.

## Ví dụ phổ biến
- **Gửi yêu cầu GET đến một trang web:**
  ```bash
  curl https://www.example.com
  ```

- **Gửi yêu cầu POST với dữ liệu:**
  ```bash
  curl -X POST -d "name=John&age=30" https://www.example.com/api
  ```

- **Tải xuống tệp và lưu vào tệp cục bộ:**
  ```bash
  curl -o myfile.txt https://www.example.com/file.txt
  ```

- **Gửi yêu cầu với tiêu đề tùy chỉnh:**
  ```bash
  curl -H "Authorization: Bearer token" https://www.example.com/api
  ```

- **Chỉ nhận tiêu đề phản hồi:**
  ```bash
  curl -I https://www.example.com
  ```

## Mẹo
- Sử dụng `-v` để xem thông tin chi tiết về yêu cầu và phản hồi, giúp bạn gỡ lỗi dễ dàng hơn.
- Khi gửi dữ liệu nhạy cảm, hãy sử dụng giao thức HTTPS để bảo mật thông tin.
- Kiểm tra mã trạng thái HTTP bằng cách sử dụng tùy chọn `-w` để đảm bảo yêu cầu của bạn thành công.