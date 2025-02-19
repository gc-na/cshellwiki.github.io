# [Hệ điều hành] C Shell (csh) umask: [quản lý quyền truy cập tệp]

## Tổng quan
Lệnh `umask` trong C Shell (csh) được sử dụng để thiết lập quyền truy cập mặc định cho các tệp và thư mục mới được tạo ra. Nó xác định các quyền mà người dùng không muốn cấp cho các tệp và thư mục mới.

## Cú pháp
Cú pháp cơ bản của lệnh `umask` như sau:

```
umask [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-S`: Hiển thị giá trị umask hiện tại dưới dạng ký hiệu.
- `-p`: Hiển thị giá trị umask hiện tại mà không thay đổi nó.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `umask`:

1. **Xem giá trị umask hiện tại**:
   ```csh
   umask
   ```

2. **Thiết lập umask mới**:
   ```csh
   umask 022
   ```

3. **Hiển thị giá trị umask hiện tại dưới dạng ký hiệu**:
   ```csh
   umask -S
   ```

4. **Thiết lập umask cho phép quyền đọc và ghi cho chủ sở hữu, nhưng chỉ quyền đọc cho nhóm và người khác**:
   ```csh
   umask 133
   ```

## Mẹo
- Hãy nhớ rằng giá trị umask được áp dụng cho các tệp và thư mục mới, vì vậy hãy thiết lập nó trước khi tạo tệp hoặc thư mục mới.
- Kiểm tra giá trị umask thường xuyên để đảm bảo rằng nó phù hợp với yêu cầu bảo mật của bạn.
- Sử dụng lệnh `umask -S` để dễ dàng hiểu các quyền hiện tại mà bạn đang thiết lập.