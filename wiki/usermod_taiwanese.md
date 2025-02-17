# [Linux] Bash usermod 使用法: 用於修改使用者帳號的指令

## Overview
`usermod` 是一個用於修改現有使用者帳號的指令。透過這個指令，系統管理員可以變更使用者的屬性，例如使用者名稱、群組、家目錄等。

## Usage
基本語法如下：
```bash
usermod [options] [arguments]
```

## Common Options
- `-l, --login NEW_LOGIN`：變更使用者的登入名稱。
- `-d, --home NEW_HOME`：變更使用者的家目錄。
- `-m, --move-home`：在變更家目錄時，將舊的家目錄內容移動到新的家目錄。
- `-G, --groups GROUP1[,GROUP2,...]`：設定使用者所屬的附加群組。
- `-a, --append`：將使用者添加到附加群組時，保留原有群組。
- `-s, --shell SHELL`：變更使用者的預設 shell。

## Common Examples
以下是幾個常見的使用範例：

1. 變更使用者的登入名稱：
   ```bash
   usermod -l newusername oldusername
   ```

2. 變更使用者的家目錄：
   ```bash
   usermod -d /new/home/directory username
   ```

3. 變更使用者的家目錄並移動舊內容：
   ```bash
   usermod -d /new/home/directory -m username
   ```

4. 添加使用者到附加群組：
   ```bash
   usermod -a -G group1,group2 username
   ```

5. 變更使用者的預設 shell：
   ```bash
   usermod -s /bin/zsh username
   ```

## Tips
- 在執行 `usermod` 指令之前，建議先備份相關的使用者資料，以防止意外的資料遺失。
- 使用 `usermod` 變更使用者名稱時，請確保沒有其他進程正在使用該使用者的會話。
- 確認變更後的設定可以使用 `id username` 指令來檢查使用者的屬性。