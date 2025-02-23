# [中文] Debian Almquist Shell (dash) umask 使用方法: 设置文件权限掩码

## 概述
`umask` 命令用于设置新创建文件和目录的默认权限掩码。它决定了在创建文件时，哪些权限将被禁用，从而影响文件和目录的可访问性。

## 用法
基本语法如下：
```
umask [选项] [参数]
```

## 常用选项
- `-S`：以符号形式显示当前的 umask 值。
- `-p`：显示当前 umask 值并保持当前设置不变。

## 常见示例
1. **查看当前 umask 值**
   ```sh
   umask
   ```

2. **设置 umask 值为 022**
   ```sh
   umask 022
   ```
   这将使新创建的文件权限为 644（rw-r--r--），目录权限为 755（rwxr-xr-x）。

3. **以符号形式查看 umask 值**
   ```sh
   umask -S
   ```

4. **设置 umask 值为 007**
   ```sh
   umask 007
   ```
   这将使新创建的文件和目录仅对用户和组可读写。

## 提示
- 在脚本中设置 umask 值可以确保创建的文件具有一致的权限。
- 在多用户环境中，合理设置 umask 值可以提高系统安全性，防止不必要的文件访问。
- 使用 `umask -S` 可以帮助你更直观地理解当前的权限设置。