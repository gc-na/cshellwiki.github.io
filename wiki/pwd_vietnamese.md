# [Hệ điều hành Unix] C Shell (csh) pwd Cách sử dụng: Xác định thư mục hiện tại

## Tổng quan
Lệnh `pwd` (print working directory) trong C Shell (csh) được sử dụng để hiển thị đường dẫn tuyệt đối của thư mục hiện tại mà người dùng đang làm việc. Đây là một công cụ hữu ích để biết vị trí chính xác trong hệ thống tệp.

## Cách sử dụng
Cú pháp cơ bản của lệnh `pwd` như sau:
```
pwd [options] [arguments]
```

## Các tùy chọn phổ biến
- `-L`: Hiển thị đường dẫn logic, tức là đường dẫn mà người dùng đã truy cập.
- `-P`: Hiển thị đường dẫn vật lý, tức là đường dẫn thực tế trên hệ thống tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tiễn về cách sử dụng lệnh `pwd`:

1. Hiển thị thư mục hiện tại:
   ```csh
   pwd
   ```

2. Hiển thị đường dẫn vật lý:
   ```csh
   pwd -P
   ```

3. Hiển thị đường dẫn logic:
   ```csh
   pwd -L
   ```

## Mẹo
- Sử dụng lệnh `pwd` thường xuyên để xác định vị trí của bạn trong hệ thống tệp, đặc biệt khi làm việc với nhiều thư mục.
- Kết hợp lệnh `pwd` với các lệnh khác như `cd` để dễ dàng điều hướng trong hệ thống tệp.
- Hãy nhớ rằng lệnh `pwd` không yêu cầu bất kỳ tham số nào, vì vậy bạn có thể sử dụng nó một cách nhanh chóng và dễ dàng.