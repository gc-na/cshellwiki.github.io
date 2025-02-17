# [Linux] Bash shift cách sử dụng: Di chuyển các tham số

## Overview
Lệnh `shift` trong Bash được sử dụng để di chuyển các tham số trong một tập hợp các tham số. Khi bạn gọi lệnh này, nó sẽ loại bỏ tham số đầu tiên và dịch chuyển tất cả các tham số còn lại sang trái, giúp bạn dễ dàng xử lý các tham số trong các kịch bản phức tạp.

## Usage
Cú pháp cơ bản của lệnh `shift` như sau:
```
shift [n]
```
Trong đó `n` là số lượng tham số bạn muốn dịch chuyển. Nếu không chỉ định `n`, lệnh sẽ mặc định dịch chuyển một tham số.

## Common Options
- `n`: Số lượng tham số sẽ được dịch chuyển. Nếu không có `n`, mặc định là 1.

## Common Examples

### Ví dụ 1: Dịch chuyển một tham số
```bash
#!/bin/bash
echo "Tham số ban đầu: $1 $2 $3"
shift
echo "Sau khi shift: $1 $2 $3"
```
Kết quả sẽ là:
```
Tham số ban đầu: thamso1 thamso2 thamso3
Sau khi shift: thamso2 thamso3
```

### Ví dụ 2: Dịch chuyển hai tham số
```bash
#!/bin/bash
echo "Tham số ban đầu: $1 $2 $3"
shift 2
echo "Sau khi shift 2: $1 $2 $3"
```
Kết quả sẽ là:
```
Tham số ban đầu: thamso1 thamso2 thamso3
Sau khi shift 2: thamso3
```

### Ví dụ 3: Sử dụng trong vòng lặp
```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "Xử lý tham số: $1"
    shift
done
```
Khi chạy với các tham số, ví dụ `./script.sh thamso1 thamso2 thamso3`, kết quả sẽ là:
```
Xử lý tham số: thamso1
Xử lý tham số: thamso2
Xử lý tham số: thamso3
```

## Tips
- Sử dụng `shift` trong các vòng lặp để dễ dàng xử lý từng tham số một cách tuần tự.
- Hãy cẩn thận với số lượng tham số bạn dịch chuyển, vì nếu bạn dịch chuyển nhiều hơn số tham số hiện có, Bash sẽ không báo lỗi nhưng các tham số sẽ trở thành trống.
- Kết hợp `shift` với các cấu trúc điều kiện để xử lý tham số một cách linh hoạt hơn.