# [Linux] Bash break cách sử dụng: Dừng vòng lặp

## Overview
Lệnh `break` trong Bash được sử dụng để thoát khỏi một vòng lặp, chẳng hạn như vòng lặp `for`, `while`, hoặc `until`. Khi lệnh `break` được thực thi, chương trình sẽ dừng lại ngay lập tức và tiếp tục với lệnh tiếp theo sau vòng lặp.

## Usage
Cú pháp cơ bản của lệnh `break` như sau:
```bash
break [n]
```
Trong đó, `n` là số lượng vòng lặp cần thoát. Nếu không chỉ định `n`, lệnh sẽ thoát khỏi vòng lặp gần nhất.

## Common Options
- `n`: Số lượng vòng lặp cần thoát. Nếu `n` được chỉ định, `break` sẽ thoát khỏi vòng lặp thứ `n` từ trong ra ngoài.

## Common Examples
### Ví dụ 1: Thoát khỏi vòng lặp `for`
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo "Số: $i"
done
```
Kết quả:
```
Số: 1
Số: 2
```

### Ví dụ 2: Thoát khỏi vòng lặp `while`
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 4 ]; then
    break
  fi
  echo "Đếm: $count"
  ((count++))
done
```
Kết quả:
```
Đếm: 1
Đếm: 2
Đếm: 3
```

### Ví dụ 3: Thoát khỏi vòng lặp lồng nhau
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "i: $i, j: $j"
  done
done
```
Kết quả:
```
i: 1, j: 1
```

## Tips
- Sử dụng `break` để kiểm soát luồng chương trình trong các vòng lặp phức tạp.
- Khi làm việc với vòng lặp lồng nhau, hãy chỉ định số lượng vòng lặp cần thoát để tránh nhầm lẫn.
- Kết hợp `break` với các điều kiện để tạo ra các vòng lặp linh hoạt và hiệu quả hơn.