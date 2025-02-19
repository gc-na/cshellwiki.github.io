# [Hệ điều hành] C Shell (csh) 7z Cách sử dụng: Nén và giải nén tệp tin

## Tổng quan
Lệnh `7z` là một công cụ mạnh mẽ dùng để nén và giải nén các tệp tin. Nó hỗ trợ nhiều định dạng nén khác nhau và thường được sử dụng để tiết kiệm dung lượng lưu trữ hoặc để dễ dàng chia sẻ tệp tin.

## Cách sử dụng
Cú pháp cơ bản của lệnh `7z` như sau:
```
7z [options] [arguments]
```

## Các tùy chọn phổ biến
- `a`: Thêm tệp tin vào một tệp nén.
- `x`: Giải nén tệp tin.
- `l`: Liệt kê nội dung của tệp nén.
- `d`: Xóa tệp tin trong tệp nén.
- `t`: Kiểm tra tính toàn vẹn của tệp nén.

## Ví dụ phổ biến
- Nén một thư mục:
  ```bash
  7z a archive.7z /path/to/directory
  ```

- Giải nén một tệp nén:
  ```bash
  7z x archive.7z
  ```

- Liệt kê nội dung của tệp nén:
  ```bash
  7z l archive.7z
  ```

- Xóa một tệp tin trong tệp nén:
  ```bash
  7z d archive.7z file.txt
  ```

- Kiểm tra tính toàn vẹn của tệp nén:
  ```bash
  7z t archive.7z
  ```

## Mẹo
- Luôn kiểm tra tính toàn vẹn của tệp nén sau khi giải nén để đảm bảo không có lỗi xảy ra.
- Sử dụng tùy chọn `-p` để đặt mật khẩu cho tệp nén nhằm bảo vệ dữ liệu nhạy cảm.
- Thực hiện nén tệp tin với mức độ nén cao hơn bằng cách thêm tùy chọn `-mx=9` vào lệnh nén.