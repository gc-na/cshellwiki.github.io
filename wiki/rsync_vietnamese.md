# [Linux] Bash rsync Cách sử dụng: Đồng bộ hóa tệp và thư mục

## Tổng quan
Lệnh `rsync` là một công cụ mạnh mẽ dùng để đồng bộ hóa và sao chép tệp và thư mục giữa các vị trí khác nhau, có thể là trên cùng một máy tính hoặc giữa các máy tính khác nhau qua mạng. Nó rất hiệu quả trong việc chỉ sao chép những thay đổi, giúp tiết kiệm băng thông và thời gian.

## Cách sử dụng
Cú pháp cơ bản của lệnh `rsync` như sau:

```bash
rsync [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Chế độ lưu trữ, sao chép tệp và thư mục với tất cả các thuộc tính.
- `-v`: Hiển thị thông tin chi tiết trong quá trình sao chép.
- `-z`: Nén dữ liệu trong quá trình truyền tải để tiết kiệm băng thông.
- `-r`: Sao chép thư mục một cách đệ quy.
- `--delete`: Xóa các tệp trong thư mục đích mà không còn tồn tại trong thư mục nguồn.

## Ví dụ phổ biến
1. Sao chép một thư mục từ máy tính cục bộ đến máy chủ từ xa:
   ```bash
   rsync -avz /path/to/local/dir user@remote:/path/to/remote/dir
   ```

2. Đồng bộ hóa một thư mục từ máy chủ từ xa về máy tính cục bộ:
   ```bash
   rsync -avz user@remote:/path/to/remote/dir /path/to/local/dir
   ```

3. Sao chép tệp và xóa các tệp không còn tồn tại trong thư mục nguồn:
   ```bash
   rsync -av --delete /path/to/local/dir/ user@remote:/path/to/remote/dir
   ```

4. Sao chép tệp từ một máy tính cục bộ đến một thư mục khác trên cùng một máy tính:
   ```bash
   rsync -av /path/to/source/file /path/to/destination/
   ```

## Mẹo
- Luôn kiểm tra các tệp sẽ được sao chép bằng cách sử dụng tùy chọn `-n` (dry run) trước khi thực hiện lệnh thực tế.
- Sử dụng `--progress` để theo dõi tiến trình sao chép, đặc biệt là khi làm việc với các tệp lớn.
- Đảm bảo rằng bạn có quyền truy cập cần thiết trên cả nguồn và đích để tránh lỗi trong quá trình sao chép.