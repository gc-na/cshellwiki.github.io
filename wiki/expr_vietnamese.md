# [Linux] Bash expr cách sử dụng: Tính toán và so sánh

## Overview
Lệnh `expr` trong Bash được sử dụng để thực hiện các phép toán số học, so sánh và chuỗi. Nó cho phép người dùng thực hiện các phép toán đơn giản và trả về kết quả.

## Usage
Cú pháp cơ bản của lệnh `expr` như sau:
```bash
expr [options] [arguments]
```

## Common Options
- `+`: Phép cộng.
- `-`: Phép trừ.
- `*`: Phép nhân (cần phải được thoát bằng dấu `\` hoặc đặt trong dấu nháy đơn).
- `/`: Phép chia.
- `%`: Phép chia lấy dư.
- `=`: So sánh bằng.
- `!=`: So sánh không bằng.
- `<`: So sánh nhỏ hơn.
- `>`: So sánh lớn hơn.

## Common Examples
- **Phép cộng hai số:**
```bash
expr 5 + 3
```
Kết quả: `8`

- **Phép trừ hai số:**
```bash
expr 10 - 4
```
Kết quả: `6`

- **Phép nhân hai số:**
```bash
expr 4 \* 7
```
Kết quả: `28`

- **Phép chia hai số:**
```bash
expr 20 / 4
```
Kết quả: `5`

- **So sánh hai số:**
```bash
expr 5 = 5
```
Kết quả: `1` (đúng)

- **So sánh không bằng:**
```bash
expr 5 != 3
```
Kết quả: `1` (đúng)

## Tips
- Khi sử dụng phép nhân với `*`, hãy nhớ thoát ký tự bằng dấu `\` hoặc sử dụng dấu nháy đơn để tránh lỗi cú pháp.
- `expr` chỉ hỗ trợ các phép toán số học và so sánh đơn giản, nếu cần thực hiện các phép toán phức tạp hơn, hãy xem xét sử dụng các công cụ khác như `bc` hoặc `awk`.
- Luôn kiểm tra kết quả của lệnh `expr` để đảm bảo rằng các phép toán được thực hiện chính xác.