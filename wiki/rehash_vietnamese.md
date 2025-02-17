# [Linux] Bash rehash cách sử dụng: Cập nhật danh sách lệnh

## Tổng quan
Lệnh `rehash` trong Bash được sử dụng để cập nhật danh sách các lệnh có sẵn trong shell. Khi bạn cài đặt hoặc xóa các chương trình, lệnh này giúp shell nhận diện các thay đổi đó mà không cần khởi động lại phiên làm việc.

## Cách sử dụng
Cú pháp cơ bản của lệnh `rehash` như sau:

```
rehash [options] [arguments]
```

## Các tùy chọn phổ biến
- Không có tùy chọn đặc biệt nào cho lệnh `rehash`. Lệnh này thường được sử dụng mà không có tham số bổ sung.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `rehash`:

1. **Cập nhật danh sách lệnh sau khi cài đặt một chương trình mới:**
   ```bash
   rehash
   ```

2. **Sử dụng `rehash` sau khi xóa một chương trình:**
   ```bash
   rehash
   ```

3. **Kiểm tra xem lệnh đã được cập nhật hay chưa:**
   ```bash
   rehash
   command -v <tên_lệnh_mới>
   ```

## Mẹo
- **Thường xuyên sử dụng:** Nếu bạn thường xuyên cài đặt hoặc gỡ bỏ các chương trình, hãy nhớ sử dụng `rehash` để đảm bảo shell của bạn luôn nhận diện được các lệnh mới.
- **Kết hợp với alias:** Nếu bạn sử dụng alias cho các lệnh, hãy chạy `rehash` sau khi tạo hoặc thay đổi alias để đảm bảo chúng được nhận diện.
- **Kiểm tra lệnh:** Sau khi sử dụng `rehash`, bạn có thể kiểm tra xem lệnh mới đã được nhận diện bằng cách sử dụng `command -v <tên_lệnh>`.