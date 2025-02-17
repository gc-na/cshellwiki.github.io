# [台灣] Bash popd 用法: 回到先前的目錄

## Overview
`popd` 命令用於從目錄堆疊中移除目錄，並切換到該目錄。這個命令通常與 `pushd` 一起使用，後者用來將當前目錄推入堆疊。

## Usage
基本語法如下：
```
popd [options]
```

## Common Options
- `-n`：不改變當前目錄，只是從堆疊中移除目錄。
- `+N`：從堆疊中移動到指定的目錄，N 是堆疊中的索引。
- `-N`：從堆疊中移動到倒數第 N 個目錄。

## Common Examples
以下是一些常見的使用範例：

1. **基本使用**
   ```bash
   pushd /path/to/directory
   popd
   ```
   這將切換回之前的目錄。

2. **使用 -n 選項**
   ```bash
   pushd /path/to/directory
   popd -n
   ```
   這將從堆疊中移除目錄，但不會切換到該目錄。

3. **使用 +N 選項**
   ```bash
   pushd /path/to/first
   pushd /path/to/second
   pushd /path/to/third
   popd +1
   ```
   這將切換到堆疊中的第二個目錄。

4. **使用 -N 選項**
   ```bash
   pushd /path/to/first
   pushd /path/to/second
   pushd /path/to/third
   popd -1
   ```
   這將切換到倒數第二個目錄。

## Tips
- 使用 `pushd` 和 `popd` 可以方便地在多個目錄之間切換，特別是在處理大型專案時。
- 可以使用 `dirs` 命令查看當前的目錄堆疊，這樣可以更好地管理目錄。
- 結合使用 `pushd` 和 `popd` 可以提高工作效率，減少輸入路徑的時間。