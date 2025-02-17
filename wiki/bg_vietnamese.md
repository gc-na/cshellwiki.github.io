# [Linux] Bash bg Cách sử dụng: Chuyển tiến trình sang chế độ nền

## Overview
Lệnh `bg` trong Bash được sử dụng để chuyển một tiến trình đang chạy trong chế độ nền. Khi bạn chạy một lệnh trong chế độ nền, nó sẽ tiếp tục hoạt động mà không chiếm dụng terminal của bạn, cho phép bạn thực hiện các tác vụ khác.

## Usage
Cú pháp cơ bản của lệnh `bg` như sau:
```bash
bg [options] [job_spec]
```

## Common Options
- `job_spec`: Chỉ định tiến trình mà bạn muốn chuyển sang chế độ nền. Bạn có thể sử dụng số thứ tự của tiến trình hoặc ký hiệu `%` để chỉ định.
- `-n`: Không gửi thông báo khi tiến trình bắt đầu chạy trong chế độ nền.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `bg`:

1. **Chuyển tiến trình gần nhất sang chế độ nền**:
   ```bash
   bg
   ```

2. **Chuyển một tiến trình cụ thể sang chế độ nền**:
   ```bash
   bg %1
   ```

3. **Chuyển tiến trình thứ hai sang chế độ nền**:
   ```bash
   bg %2
   ```

4. **Chuyển tiến trình với thông báo**:
   ```bash
   bg -n %1
   ```

## Tips
- Để xem danh sách các tiến trình đang chạy, bạn có thể sử dụng lệnh `jobs`.
- Nếu bạn muốn dừng một tiến trình trước khi chuyển nó sang chế độ nền, bạn có thể sử dụng lệnh `Ctrl + Z` để tạm dừng tiến trình đó.
- Hãy chắc chắn rằng bạn đã kiểm tra trạng thái của tiến trình bằng lệnh `jobs` sau khi sử dụng `bg` để đảm bảo rằng nó đã được chuyển thành công sang chế độ nền.