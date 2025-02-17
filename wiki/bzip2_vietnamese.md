# [Linux] Bash bzip2 Cách sử dụng: Nén và giải nén tệp tin

## Tổng quan
Lệnh `bzip2` là một công cụ dùng để nén và giải nén các tệp tin. Nó sử dụng thuật toán nén bzip2, giúp giảm kích thước tệp tin một cách hiệu quả, thường được sử dụng cho các tệp lớn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `bzip2` như sau:

```bash
bzip2 [options] [arguments]
```

## Tùy chọn phổ biến
- `-d`, `--decompress`: Giải nén tệp tin.
- `-k`, `--keep`: Giữ lại tệp tin gốc sau khi nén.
- `-f`, `--force`: Ghi đè lên tệp tin đã tồn tại mà không hỏi.
- `-v`, `--verbose`: Hiển thị thông tin chi tiết trong quá trình nén hoặc giải nén.
- `-z`, `--compress`: Nén tệp tin (mặc định).

## Ví dụ phổ biến
- Nén một tệp tin:
```bash
bzip2 file.txt
```

- Giải nén một tệp tin đã nén:
```bash
bzip2 -d file.txt.bz2
```

- Nén tệp tin và giữ lại tệp gốc:
```bash
bzip2 -k file.txt
```

- Nén nhiều tệp tin cùng một lúc:
```bash
bzip2 file1.txt file2.txt
```

- Hiển thị thông tin chi tiết trong quá trình nén:
```bash
bzip2 -v file.txt
```

## Mẹo
- Luôn kiểm tra kích thước tệp tin sau khi nén để đảm bảo rằng việc nén đã thành công.
- Sử dụng tùy chọn `-k` nếu bạn cần giữ lại bản gốc của tệp tin.
- Đối với các tệp tin lớn, hãy cân nhắc sử dụng `pbzip2` để tận dụng đa luồng, giúp tăng tốc độ nén.