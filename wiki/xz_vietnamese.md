# [Hệ điều hành] C Shell (csh) xz: Nén và giải nén tệp tin

## Tổng quan
Lệnh `xz` được sử dụng để nén và giải nén các tệp tin, giúp giảm kích thước tệp để tiết kiệm không gian lưu trữ. Nó sử dụng thuật toán nén LZMA, mang lại hiệu suất nén cao.

## Cách sử dụng
Cú pháp cơ bản của lệnh `xz` như sau:
```bash
xz [options] [arguments]
```

## Các tùy chọn phổ biến
- `-d`, `--decompress`: Giải nén tệp tin.
- `-k`, `--keep`: Giữ lại tệp tin gốc sau khi nén.
- `-v`, `--verbose`: Hiển thị thông tin chi tiết trong quá trình nén hoặc giải nén.
- `-f`, `--force`: Buộc ghi đè lên các tệp tin đã tồn tại.

## Ví dụ thường gặp
- Nén một tệp tin:
```bash
xz filename.txt
```
- Giải nén một tệp tin đã nén:
```bash
xz -d filename.txt.xz
```
- Nén tệp tin và giữ lại tệp gốc:
```bash
xz -k filename.txt
```
- Hiển thị thông tin chi tiết khi nén:
```bash
xz -v filename.txt
```

## Mẹo
- Luôn kiểm tra kích thước tệp sau khi nén để đảm bảo rằng quá trình nén diễn ra thành công.
- Sử dụng tùy chọn `-k` nếu bạn muốn giữ lại bản gốc của tệp tin để tránh mất dữ liệu.
- Đối với các tệp tin lớn, hãy cân nhắc sử dụng `xz` với các tùy chọn nén cao hơn để tối ưu hóa không gian lưu trữ.