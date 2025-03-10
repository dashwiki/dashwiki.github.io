# [中文] Debian Almquist Shell (dash) rm 用法: 删除文件和目录

## 概述
`rm` 命令用于删除文件和目录。它是一个强大的工具，能够永久性地移除指定的文件或目录，因此在使用时需要格外小心。

## 用法
基本语法如下：
```
rm [选项] [参数]
```

## 常用选项
- `-f`：强制删除，不提示用户确认。
- `-i`：在删除每个文件之前提示确认。
- `-r`：递归删除，用于删除目录及其内容。
- `-v`：详细模式，显示删除的文件名。

## 常见示例
1. 删除单个文件：
   ```bash
   rm file.txt
   ```

2. 强制删除文件，不提示确认：
   ```bash
   rm -f file.txt
   ```

3. 删除目录及其所有内容：
   ```bash
   rm -r directory_name
   ```

4. 在删除之前进行确认：
   ```bash
   rm -i file.txt
   ```

5. 递归删除目录并显示详细信息：
   ```bash
   rm -rv directory_name
   ```

## 提示
- 在使用 `rm` 命令时，建议先使用 `-i` 选项进行确认，以避免意外删除重要文件。
- 定期备份重要数据，确保在误删时可以恢复。
- 对于重要的目录，考虑使用 `mv` 命令将其移动到安全位置，而不是直接删除。