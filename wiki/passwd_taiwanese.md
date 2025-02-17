# [台灣] Bash passwd 用法: 修改使用者密碼

## Overview
`passwd` 命令用於修改使用者的密碼。這個命令可以讓使用者更新自己的密碼，或是由管理員為其他使用者設定密碼。

## Usage
基本語法如下：
```bash
passwd [options] [username]
```

## Common Options
- `-d`: 刪除使用者的密碼，讓其無法使用密碼登入。
- `-e`: 立即過期使用者的密碼，使用者下次登入時必須更改密碼。
- `-l`: 鎖定使用者帳戶，禁止登入。
- `-u`: 解鎖使用者帳戶，允許登入。
- `-S`: 顯示使用者的密碼狀態。

## Common Examples
- 修改當前使用者的密碼：
  ```bash
  passwd
  ```

- 修改指定使用者的密碼（需要管理員權限）：
  ```bash
  sudo passwd username
  ```

- 刪除使用者的密碼：
  ```bash
  sudo passwd -d username
  ```

- 鎖定使用者帳戶：
  ```bash
  sudo passwd -l username
  ```

- 解鎖使用者帳戶：
  ```bash
  sudo passwd -u username
  ```

## Tips
- 在設定新密碼時，確保使用強密碼以提高安全性。
- 定期更改密碼可以增強帳戶的安全性。
- 使用 `passwd -S username` 可以檢查使用者的密碼狀態，了解其是否被鎖定或過期。