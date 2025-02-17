# [Linux] Bash continue sử dụng: Tiếp tục vòng lặp

## Overview
Lệnh `continue` trong Bash được sử dụng để bỏ qua phần còn lại của vòng lặp hiện tại và tiếp tục với lần lặp tiếp theo. Điều này rất hữu ích khi bạn muốn bỏ qua một số điều kiện nhất định trong vòng lặp mà không thoát khỏi toàn bộ vòng lặp.

## Usage
Cú pháp cơ bản của lệnh `continue` như sau:
```
continue [n]
```
Trong đó `n` là số lần lặp mà bạn muốn bỏ qua. Nếu không chỉ định `n`, lệnh sẽ bỏ qua phần còn lại của vòng lặp hiện tại và tiếp tục với lần lặp tiếp theo.

## Common Options
- `n`: Số lần lặp mà bạn muốn bỏ qua. Nếu không có tham số này, lệnh sẽ tiếp tục với lần lặp ngay sau.

## Common Examples

### Ví dụ 1: Bỏ qua số chẵn trong vòng lặp
```bash
for i in {1..10}; do
  if (( i % 2 == 0 )); then
    continue
  fi
  echo $i
done
```
Kết quả: 
```
1
3
5
7
9
```
Trong ví dụ này, lệnh `continue` sẽ bỏ qua các số chẵn và chỉ in ra các số lẻ.

### Ví dụ 2: Bỏ qua vòng lặp khi gặp điều kiện
```bash
for file in *; do
  if [[ $file == *.tmp ]]; then
    continue
  fi
  echo "Processing $file"
done
```
Kết quả: 
```
Processing file1.txt
Processing file2.log
```
Ở đây, lệnh `continue` sẽ bỏ qua các tệp có đuôi `.tmp`.

### Ví dụ 3: Sử dụng với `while`
```bash
count=1
while [ $count -le 10 ]; do
  (( count % 3 == 0 )) && continue
  echo $count
  ((count++))
done
```
Kết quả: 
```
1
2
4
5
7
8
10
```
Trong ví dụ này, các số chia hết cho 3 sẽ bị bỏ qua.

## Tips
- Sử dụng `continue` để làm cho mã của bạn dễ đọc hơn bằng cách giảm thiểu việc lồng ghép các điều kiện.
- Hãy cẩn thận khi sử dụng `continue` trong các vòng lặp lồng nhau, vì nó chỉ ảnh hưởng đến vòng lặp hiện tại.
- Kiểm tra kỹ các điều kiện trước khi sử dụng `continue` để đảm bảo rằng bạn không bỏ qua những lần lặp quan trọng.