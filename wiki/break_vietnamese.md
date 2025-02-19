# [Hệ điều hành] C Shell (csh) break Cách sử dụng: Dừng vòng lặp

## Overview
Lệnh `break` trong C Shell (csh) được sử dụng để thoát khỏi một vòng lặp. Khi lệnh này được thực thi, nó sẽ dừng vòng lặp hiện tại và tiếp tục với lệnh tiếp theo sau vòng lặp.

## Usage
Cú pháp cơ bản của lệnh `break` như sau:

```
break [options]
```

## Common Options
Lệnh `break` không có nhiều tùy chọn. Tuy nhiên, bạn có thể sử dụng nó trong các vòng lặp như `foreach`, `while`, hoặc `for`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `break`:

### Ví dụ 1: Dừng vòng lặp `while`
```csh
set count = 1
while ($count <= 5)
    echo "Count is $count"
    if ($count == 3) then
        break
    endif
    @ count++
end
```

### Ví dụ 2: Dừng vòng lặp `foreach`
```csh
foreach item (apple banana cherry)
    if ("$item" == "banana") then
        break
    endif
    echo "Current item: $item"
end
```

### Ví dụ 3: Sử dụng trong vòng lặp `for`
```csh
foreach i (1 2 3 4 5)
    if ($i == 4) then
        break
    endif
    echo "Number: $i"
end
```

## Tips
- Sử dụng `break` khi bạn cần dừng vòng lặp sớm trong các tình huống cụ thể.
- Kết hợp `break` với các điều kiện để kiểm soát luồng thực thi của chương trình một cách hiệu quả hơn.
- Hãy chắc chắn rằng bạn hiểu rõ cấu trúc của vòng lặp để sử dụng `break` một cách hợp lý.