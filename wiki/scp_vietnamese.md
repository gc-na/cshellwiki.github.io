# [Hệ điều hành] C Shell (csh) scp cách sử dụng: Chuyển file an toàn giữa các máy tính

## Tổng quan
Lệnh `scp` (Secure Copy Protocol) cho phép bạn sao chép file hoặc thư mục giữa các máy tính qua mạng một cách an toàn. Nó sử dụng giao thức SSH để đảm bảo rằng dữ liệu được truyền tải một cách bảo mật.

## Cách sử dụng
Cú pháp cơ bản của lệnh `scp` như sau:
```csh
scp [options] [arguments]
```

## Các tùy chọn phổ biến
- `-r`: Sao chép thư mục và tất cả các file bên trong.
- `-P port`: Chỉ định cổng SSH khác với cổng mặc định (22).
- `-i identity_file`: Sử dụng file khóa riêng để xác thực.
- `-v`: Chế độ chi tiết, hiển thị thông tin về quá trình sao chép.

## Ví dụ phổ biến
- Sao chép file từ máy cục bộ đến máy từ xa:
```csh
scp localfile.txt user@remotehost:/path/to/destination/
```
- Sao chép file từ máy từ xa về máy cục bộ:
```csh
scp user@remotehost:/path/to/remotefile.txt /local/destination/
```
- Sao chép thư mục từ máy cục bộ đến máy từ xa:
```csh
scp -r localfolder user@remotehost:/path/to/destination/
```
- Sao chép file qua cổng SSH khác:
```csh
scp -P 2222 localfile.txt user@remotehost:/path/to/destination/
```

## Mẹo
- Luôn kiểm tra kết nối SSH trước khi sử dụng `scp` để đảm bảo rằng bạn có quyền truy cập vào máy từ xa.
- Sử dụng tùy chọn `-v` để gỡ lỗi nếu có vấn đề xảy ra trong quá trình sao chép.
- Nếu bạn thường xuyên sao chép file đến cùng một máy, hãy xem xét việc thiết lập xác thực bằng khóa SSH để tiết kiệm thời gian nhập mật khẩu.