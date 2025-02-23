# [中文] Debian Almquist Shell (dash) iotop 用法: 监控磁盘I/O使用情况

## 概述
iotop 是一个用于实时监控系统中磁盘I/O使用情况的命令行工具。它可以显示哪些进程正在进行磁盘读写操作，以及它们的I/O速率，帮助用户识别和诊断I/O瓶颈。

## 用法
基本语法如下：
```bash
iotop [options] [arguments]
```

## 常用选项
- `-o`：仅显示当前有I/O活动的进程。
- `-b`：以批处理模式运行，适合输出到文件。
- `-n NUM`：指定输出的更新次数。
- `-d SEC`：设置更新的时间间隔（以秒为单位）。

## 常见示例
1. 实时监控I/O活动：
   ```bash
   iotop
   ```

2. 仅显示有I/O活动的进程：
   ```bash
   iotop -o
   ```

3. 以批处理模式运行并输出到文件：
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. 设置更新间隔为2秒，并显示5次更新：
   ```bash
   iotop -d 2 -n 5
   ```

## 小贴士
- 在使用 `iotop` 时，确保你有足够的权限，通常需要以 root 用户身份运行。
- 使用 `-b` 选项可以将输出重定向到文件，方便后续分析。
- 定期检查I/O活动可以帮助你识别性能问题，及时调整系统配置。