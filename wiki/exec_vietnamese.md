# [Linux] Bash exec cách sử dụng: Thay thế tiến trình hiện tại

## Tổng quan
Lệnh `exec` trong Bash được sử dụng để thay thế tiến trình hiện tại bằng một tiến trình mới. Khi bạn sử dụng `exec`, tiến trình hiện tại sẽ bị chấm dứt và được thay thế hoàn toàn bởi tiến trình mà bạn chỉ định.

## Cách sử dụng
Cú pháp cơ bản của lệnh `exec` như sau:

```bash
exec [options] [arguments]
```

## Tùy chọn phổ biến
- `-a`: Chỉ định tên cho tiến trình mới.
- `-l`: Thực thi lệnh như một shell đăng nhập.
- `-c`: Bỏ qua các biến môi trường hiện tại.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `exec`:

1. **Thay thế shell hiện tại bằng một shell mới**:
   ```bash
   exec bash
   ```

2. **Chạy một chương trình và thay thế shell hiện tại**:
   ```bash
   exec /path/to/program
   ```

3. **Chạy một lệnh với tên tùy chỉnh**:
   ```bash
   exec -a custom_name /path/to/program
   ```

4. **Sử dụng exec để chạy một lệnh trong một shell đăng nhập**:
   ```bash
   exec -l bash
   ```

## Mẹo
- Sử dụng `exec` khi bạn muốn tiết kiệm tài nguyên hệ thống bằng cách không giữ lại tiến trình shell cũ.
- Hãy cẩn thận khi sử dụng `exec` vì nó sẽ chấm dứt tiến trình hiện tại; đảm bảo rằng bạn không cần tiến trình đó sau khi thực hiện lệnh.
- Bạn có thể kiểm tra mã thoát của lệnh vừa chạy bằng cách sử dụng `$?` ngay sau khi lệnh `exec` được thực hiện.