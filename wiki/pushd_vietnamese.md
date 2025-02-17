# [Linux] Bash pushd cách sử dụng: Lệnh chuyển đổi thư mục

## Overview
Lệnh `pushd` trong Bash được sử dụng để chuyển đổi giữa các thư mục và lưu trữ thư mục hiện tại vào ngăn xếp. Điều này cho phép bạn dễ dàng quay lại thư mục trước đó bằng cách sử dụng lệnh `popd`.

## Usage
Cú pháp cơ bản của lệnh `pushd` như sau:

```bash
pushd [options] [arguments]
```

## Common Options
- `+n`: Chuyển đến thư mục thứ n trong ngăn xếp.
- `-n`: Chỉ thay đổi thư mục mà không thay đổi thư mục hiện tại.
- `-`: Quay lại thư mục trước đó trong ngăn xếp.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `pushd`:

### Ví dụ 1: Chuyển đến thư mục mới
```bash
pushd /path/to/directory
```
Lệnh này sẽ chuyển đến thư mục `/path/to/directory` và lưu thư mục hiện tại vào ngăn xếp.

### Ví dụ 2: Quay lại thư mục trước đó
```bash
popd
```
Lệnh này sẽ quay lại thư mục trước đó mà bạn đã lưu trong ngăn xếp.

### Ví dụ 3: Chuyển đến thư mục thứ hai trong ngăn xếp
```bash
pushd +1
```
Lệnh này sẽ chuyển đến thư mục thứ hai trong ngăn xếp.

### Ví dụ 4: Chuyển đến thư mục và không thay đổi thư mục hiện tại
```bash
pushd -n /another/path
```
Lệnh này sẽ chỉ thay đổi ngăn xếp mà không thay đổi thư mục hiện tại.

## Tips
- Sử dụng `dirs` để xem danh sách các thư mục trong ngăn xếp.
- Kết hợp `pushd` và `popd` để dễ dàng quản lý các thư mục khi làm việc với nhiều dự án.
- Hãy nhớ rằng ngăn xếp thư mục sẽ giữ lại các thư mục bạn đã truy cập, vì vậy bạn có thể quay lại bất kỳ lúc nào.