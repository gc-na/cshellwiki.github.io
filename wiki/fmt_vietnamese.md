# [Hệ điều hành Unix] C Shell (csh) fmt Cách sử dụng: Định dạng văn bản

## Tổng quan
Lệnh `fmt` trong C Shell (csh) được sử dụng để định dạng văn bản, giúp điều chỉnh chiều dài của các dòng trong một tệp văn bản. Lệnh này rất hữu ích khi bạn cần làm cho văn bản dễ đọc hơn bằng cách đảm bảo rằng các dòng không quá dài.

## Cách sử dụng
Cú pháp cơ bản của lệnh `fmt` như sau:

```csh
fmt [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-w <số>`: Xác định chiều dài tối đa của mỗi dòng (mặc định là 75 ký tự).
- `-s`: Bỏ qua các dòng trống khi định dạng.
- `-u`: Loại bỏ các khoảng trắng thừa ở đầu và cuối mỗi dòng.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `fmt`:

1. Định dạng tệp văn bản với chiều dài dòng mặc định:
   ```csh
   fmt input.txt
   ```

2. Định dạng tệp văn bản với chiều dài dòng tối đa là 50 ký tự:
   ```csh
   fmt -w 50 input.txt
   ```

3. Định dạng tệp văn bản và lưu kết quả vào một tệp mới:
   ```csh
   fmt input.txt > output.txt
   ```

4. Định dạng văn bản và bỏ qua các dòng trống:
   ```csh
   fmt -s input.txt
   ```

## Mẹo
- Hãy thử nghiệm với tùy chọn `-w` để tìm ra chiều dài dòng phù hợp nhất cho văn bản của bạn.
- Sử dụng lệnh `cat` để xem nhanh nội dung của tệp trước khi định dạng.
- Nếu bạn làm việc với nhiều tệp, hãy sử dụng vòng lặp để áp dụng lệnh `fmt` cho tất cả các tệp trong một thư mục.