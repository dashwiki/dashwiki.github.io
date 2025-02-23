# [台灣] Debian Almquist Shell (dash) du 使用方式: 計算磁碟使用量

## Overview
`du` 命令用於顯示檔案和目錄的磁碟使用量。它可以幫助使用者了解哪些檔案或資料夾佔用了最多的空間，從而進行有效的磁碟管理。

## Usage
基本語法如下：
```
du [options] [arguments]
```

## Common Options
- `-h`：以人類可讀的格式顯示大小（例如 KB, MB）。
- `-s`：僅顯示每個指定檔案或目錄的總計。
- `-a`：顯示所有檔案的大小，而不僅僅是目錄。
- `-c`：在輸出末尾顯示總計。

## Common Examples
1. 顯示當前目錄及其子目錄的磁碟使用量：
   ```bash
   du
   ```

2. 以人類可讀的格式顯示當前目錄的磁碟使用量：
   ```bash
   du -h
   ```

3. 顯示特定目錄的總磁碟使用量：
   ```bash
   du -sh /path/to/directory
   ```

4. 顯示所有檔案及目錄的大小：
   ```bash
   du -a
   ```

5. 顯示當前目錄及其子目錄的總計：
   ```bash
   du -ch
   ```

## Tips
- 使用 `-h` 選項可以更容易地理解磁碟使用量，特別是在處理大型檔案時。
- 結合 `sort` 命令可以按大小排序輸出，例如：
  ```bash
  du -h | sort -h
  ```
- 定期檢查磁碟使用量可以幫助你及時清理不必要的檔案，保持系統的整潔。