# [Linux] Bash timedatectl Cách sử dụng: Quản lý thời gian và ngày tháng

## Overview
Lệnh `timedatectl` được sử dụng để quản lý và kiểm tra thông tin về thời gian và ngày tháng trên hệ thống Linux. Nó cho phép người dùng điều chỉnh đồng hồ hệ thống, cấu hình múi giờ và kiểm tra trạng thái đồng bộ thời gian.

## Usage
Cú pháp cơ bản của lệnh `timedatectl` như sau:

```bash
timedatectl [options] [arguments]
```

## Common Options
- `status`: Hiển thị trạng thái hiện tại của thời gian và ngày tháng.
- `set-time`: Đặt thời gian cụ thể cho hệ thống.
- `set-timezone`: Đặt múi giờ cho hệ thống.
- `set-ntp`: Bật hoặc tắt đồng bộ hóa thời gian qua NTP (Network Time Protocol).
- `list-timezones`: Liệt kê tất cả các múi giờ có sẵn.

## Common Examples
- **Kiểm tra trạng thái thời gian và ngày tháng hiện tại:**
  ```bash
  timedatectl status
  ```

- **Đặt thời gian cụ thể (ví dụ: 15:30 ngày 1 tháng 12 năm 2023):**
  ```bash
  timedatectl set-time '2023-12-01 15:30:00'
  ```

- **Đặt múi giờ (ví dụ: Châu Á/Thành_Pho_Hồ_Chí_Minh):**
  ```bash
  timedatectl set-timezone Asia/Ho_Chi_Minh
  ```

- **Bật đồng bộ hóa thời gian qua NTP:**
  ```bash
  timedatectl set-ntp true
  ```

- **Liệt kê tất cả các múi giờ có sẵn:**
  ```bash
  timedatectl list-timezones
  ```

## Tips
- Luôn kiểm tra trạng thái thời gian sau khi thực hiện bất kỳ thay đổi nào để đảm bảo rằng hệ thống đang hoạt động đúng.
- Sử dụng lệnh `list-timezones` để tìm múi giờ chính xác trước khi đặt múi giờ cho hệ thống.
- Nếu hệ thống của bạn cần đồng bộ hóa thời gian chính xác, hãy đảm bảo rằng NTP được bật.