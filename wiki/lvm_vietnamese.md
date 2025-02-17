# [Linux] Bash lvm Sử dụng: Quản lý các khối lượng logic

## Tổng quan
Lệnh `lvm` (Logical Volume Manager) được sử dụng để quản lý các khối lượng logic trong hệ thống lưu trữ. Nó cho phép người dùng tạo, xóa, và điều chỉnh các khối lượng logic, giúp tối ưu hóa việc sử dụng không gian lưu trữ và dễ dàng quản lý các phân vùng.

## Cú pháp
Cú pháp cơ bản của lệnh `lvm` như sau:
```
lvm [options] [arguments]
```

## Các tùy chọn phổ biến
- `create`: Tạo một khối lượng logic mới.
- `remove`: Xóa một khối lượng logic.
- `extend`: Mở rộng kích thước của một khối lượng logic.
- `reduce`: Giảm kích thước của một khối lượng logic.
- `lvdisplay`: Hiển thị thông tin chi tiết về các khối lượng logic hiện có.

## Ví dụ phổ biến
1. **Tạo một khối lượng logic mới**
   ```bash
   lvm lvcreate -n my_volume -L 10G my_volume_group
   ```

2. **Xóa một khối lượng logic**
   ```bash
   lvm lvremove my_volume_group/my_volume
   ```

3. **Mở rộng kích thước của một khối lượng logic**
   ```bash
   lvm lvextend -L +5G /dev/my_volume_group/my_volume
   ```

4. **Giảm kích thước của một khối lượng logic**
   ```bash
   lvm lvreduce -L -5G /dev/my_volume_group/my_volume
   ```

5. **Hiển thị thông tin về các khối lượng logic**
   ```bash
   lvm lvdisplay
   ```

## Mẹo
- Trước khi thực hiện các thao tác giảm kích thước, hãy luôn sao lưu dữ liệu để tránh mất mát.
- Sử dụng `lvdisplay` để kiểm tra thông tin về khối lượng logic trước khi thực hiện bất kỳ thay đổi nào.
- Thực hiện các thao tác trên khối lượng logic trong thời gian không có hoạt động sử dụng để đảm bảo an toàn cho dữ liệu.