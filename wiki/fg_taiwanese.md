# [台灣] Debian Almquist Shell (dash) fg 用法: 將背景工作轉為前景工作

## Overview
`fg` 命令用於將一個在背景運行的工作轉回前景，讓使用者可以直接與該工作互動。這對於需要用戶輸入或需要監控的任務特別有用。

## Usage
基本語法如下：
```
fg [options] [job_spec]
```

## Common Options
- `job_spec`：指定要轉為前景的工作，可以是工作號碼或工作名稱。

## Common Examples
1. 將最近的背景工作轉為前景：
   ```sh
   fg
   ```

2. 將特定的工作號碼（例如，作業號碼 1）轉為前景：
   ```sh
   fg %1
   ```

3. 將名為 "my_script" 的背景工作轉為前景：
   ```sh
   fg %my_script
   ```

## Tips
- 在使用 `fg` 之前，可以使用 `jobs` 命令查看當前的背景工作及其狀態。
- 如果有多個背景工作，確保使用正確的工作號碼或名稱，以避免將錯誤的工作轉為前景。
- 使用 `Ctrl + Z` 可以暫停前景工作並將其轉為背景，隨後可以使用 `fg` 來恢復它。