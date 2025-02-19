# [Hệ điều hành] C Shell (csh) rsync Cách sử dụng: Đồng bộ hóa tệp

## Tổng quan
Lệnh `rsync` là một công cụ mạnh mẽ dùng để đồng bộ hóa và sao chép tệp giữa các máy tính hoặc giữa các thư mục trên cùng một máy. Nó cho phép bạn chỉ sao chép những phần đã thay đổi của tệp, giúp tiết kiệm băng thông và thời gian.

## Cú pháp
Cú pháp cơ bản của lệnh `rsync` như sau:
```
rsync [options] [arguments]
```

## Các tùy chọn phổ biến
- `-a`: Chế độ lưu trữ, sao chép tệp và thư mục cùng với các thuộc tính của chúng.
- `-v`: Hiển thị thông tin chi tiết về quá trình sao chép.
- `-z`: Nén dữ liệu trong quá trình truyền tải để tiết kiệm băng thông.
- `-r`: Sao chép thư mục một cách đệ quy.
- `--delete`: Xóa các tệp trong thư mục đích mà không còn tồn tại trong thư mục nguồn.

## Ví dụ phổ biến
- Sao chép một tệp từ thư mục này sang thư mục khác:
```bash
rsync -av source.txt /path/to/destination/
```

- Đồng bộ hóa một thư mục với một thư mục khác:
```bash
rsync -av /path/to/source/ /path/to/destination/
```

- Sao chép tệp từ một máy chủ từ xa:
```bash
rsync -av user@remote_host:/path/to/source/ /path/to/destination/
```

- Đồng bộ hóa và xóa các tệp không còn tồn tại trong thư mục nguồn:
```bash
rsync -av --delete /path/to/source/ /path/to/destination/
```

## Mẹo
- Luôn kiểm tra lệnh với tùy chọn `-n` (dry run) trước khi thực hiện để xem những gì sẽ xảy ra:
```bash
rsync -avn /path/to/source/ /path/to/destination/
```
- Sử dụng `-z` khi truyền tải qua mạng để giảm băng thông.
- Đảm bảo rằng bạn có quyền truy cập đầy đủ vào cả thư mục nguồn và đích để tránh lỗi trong quá trình sao chép.