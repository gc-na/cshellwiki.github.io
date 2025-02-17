# [Linux] Bash switch lệnh: Chuyển đổi giữa các giá trị

## Tổng quan
Lệnh `switch` trong Bash không phải là một lệnh độc lập mà là một cấu trúc điều kiện cho phép bạn kiểm tra một biến và thực hiện các hành động khác nhau dựa trên giá trị của biến đó. Nó giúp tổ chức mã nguồn một cách rõ ràng và dễ hiểu hơn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `switch` trong Bash như sau:

```bash
switch [biến]
case [giá trị1]:
    # Lệnh cho giá trị1
    ;;
case [giá trị2]:
    # Lệnh cho giá trị2
    ;;
...
esac
```

## Các tùy chọn phổ biến
- `case`: Xác định một giá trị mà bạn muốn kiểm tra.
- `esac`: Kết thúc cấu trúc `switch`.
- `;;`: Đánh dấu sự kết thúc của một trường hợp (case).

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `switch` trong Bash:

### Ví dụ 1: Kiểm tra ngày trong tuần
```bash
day="Thứ Hai"

case $day in
    "Thứ Hai")
        echo "Hôm nay là Thứ Hai!"
        ;;
    "Thứ Ba")
        echo "Hôm nay là Thứ Ba!"
        ;;
    "Thứ Tư")
        echo "Hôm nay là Thứ Tư!"
        ;;
    *)
        echo "Không phải ngày trong tuần!"
        ;;
esac
```

### Ví dụ 2: Kiểm tra trạng thái
```bash
status="hoàn thành"

case $status in
    "đang xử lý")
        echo "Công việc đang được xử lý."
        ;;
    "hoàn thành")
        echo "Công việc đã hoàn thành."
        ;;
    "thất bại")
        echo "Công việc đã thất bại."
        ;;
    *)
        echo "Trạng thái không xác định."
        ;;
esac
```

## Mẹo
- Sử dụng `*` trong `case` để xử lý các trường hợp không xác định.
- Đảm bảo mỗi trường hợp kết thúc bằng `;;` để tránh lỗi.
- Sử dụng các biến rõ ràng để dễ dàng theo dõi giá trị mà bạn đang kiểm tra.