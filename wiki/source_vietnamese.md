# [Linux] Bash source lệnh: Thực thi các lệnh trong tệp

## Overview
Lệnh `source` trong Bash được sử dụng để thực thi các lệnh từ một tệp kịch bản trong môi trường hiện tại của shell. Điều này có nghĩa là các biến và hàm được định nghĩa trong tệp sẽ có sẵn trong phiên làm việc hiện tại.

## Usage
Cú pháp cơ bản của lệnh `source` như sau:
```
source [tùy chọn] [tệp]
```

## Common Options
- Không có tùy chọn chính thức nào cho lệnh `source`, nhưng bạn có thể sử dụng:
  - `-` : Thường được sử dụng để chỉ định rằng tệp kịch bản nên được thực thi trong chế độ không tương tác.

## Common Examples
Dưới đây là một số ví dụ thực tiễn về cách sử dụng lệnh `source`:

1. **Thực thi một tệp kịch bản**:
   ```bash
   source myscript.sh
   ```

2. **Thực thi một tệp kịch bản với đường dẫn đầy đủ**:
   ```bash
   source /path/to/myscript.sh
   ```

3. **Tải lại tệp cấu hình `.bashrc`**:
   ```bash
   source ~/.bashrc
   ```

4. **Thực thi tệp kịch bản và truyền tham số**:
   ```bash
   source myscript.sh arg1 arg2
   ```

## Tips
- Sử dụng `source` để tải lại các thay đổi trong tệp cấu hình mà không cần khởi động lại shell.
- Đảm bảo rằng tệp kịch bản có quyền thực thi nếu bạn muốn sử dụng nó với lệnh `./` thay vì `source`.
- Kiểm tra các biến môi trường sau khi thực thi tệp kịch bản để xác nhận rằng chúng đã được thiết lập đúng cách.