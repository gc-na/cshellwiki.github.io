# [Linux] Bash vgcreate Cách sử dụng: Tạo nhóm khối lượng

## Tổng quan
Lệnh `vgcreate` được sử dụng để tạo một nhóm khối lượng (volume group) trong quản lý khối lượng logic (LVM) trên hệ thống Linux. Nhóm khối lượng cho phép bạn kết hợp nhiều thiết bị lưu trữ thành một đơn vị logic duy nhất, giúp quản lý không gian lưu trữ dễ dàng hơn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `vgcreate` như sau:

```
vgcreate [tùy chọn] [tên nhóm khối lượng] [thiết bị]
```

## Tùy chọn phổ biến
- `-s, --stripes <số>`: Số lượng stripes cho nhóm khối lượng.
- `-p, --pesize <kích thước>`: Kích thước của Physical Extents (PE) trong nhóm khối lượng.
- `-n, --noudevsync`: Không đồng bộ thiết bị trong nhóm khối lượng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `vgcreate`:

1. Tạo một nhóm khối lượng mới có tên là `vg01` từ thiết bị `/dev/sdb1`:
   ```bash
   vgcreate vg01 /dev/sdb1
   ```

2. Tạo một nhóm khối lượng với kích thước PE là 32MB:
   ```bash
   vgcreate -p 32M vg02 /dev/sdc1
   ```

3. Tạo một nhóm khối lượng với nhiều thiết bị:
   ```bash
   vgcreate vg03 /dev/sdd1 /dev/sde1
   ```

## Mẹo
- Trước khi tạo nhóm khối lượng, hãy đảm bảo rằng các thiết bị đã được định dạng và không chứa dữ liệu quan trọng.
- Sử dụng lệnh `vgs` để kiểm tra thông tin về các nhóm khối lượng đã tạo.
- Đặt tên nhóm khối lượng một cách có tổ chức để dễ dàng quản lý và nhận diện trong tương lai.