# [中文] Debian Almquist Shell (dash) unxz 使用方法: 解压缩 .xz 文件

## 概述
`unxz` 命令用于解压缩 `.xz` 格式的压缩文件。它是 `xz` 工具集的一部分，能够有效地处理高压缩比的文件。

## 用法
基本语法如下：
```
unxz [选项] [参数]
```

## 常用选项
- `-k`：保留原始的 `.xz` 文件。
- `-f`：强制解压缩，即使目标文件已存在。
- `-v`：显示详细的解压缩过程。

## 常见示例
以下是一些常用的 `unxz` 示例：

1. 解压缩一个文件：
   ```bash
   unxz example.xz
   ```

2. 解压缩并保留原始文件：
   ```bash
   unxz -k example.xz
   ```

3. 强制解压缩已存在的文件：
   ```bash
   unxz -f example.xz
   ```

4. 显示详细解压缩信息：
   ```bash
   unxz -v example.xz
   ```

## 提示
- 在解压缩大文件时，确保有足够的磁盘空间。
- 使用 `-k` 选项可以在解压缩后保留原始文件，适合需要多次使用的场景。
- 如果不确定解压缩的结果，可以先使用 `-v` 选项查看详细信息。