# [中文] Debian Almquist Shell (dash) whoami 用法等价: 显示当前用户的用户名

## 概述
`whoami` 命令用于显示当前登录用户的用户名。它是一个简单而实用的命令，通常用于确认你当前以哪个用户身份在系统上操作。

## 用法
基本语法如下：
```bash
whoami [options] [arguments]
```

## 常见选项
- `--help`：显示帮助信息。
- `--version`：显示版本信息。

## 常见示例
以下是一些常用的 `whoami` 示例：

1. 显示当前用户的用户名：
   ```bash
   whoami
   ```

2. 显示当前用户的用户名并获取帮助信息：
   ```bash
   whoami --help
   ```

3. 显示当前用户的用户名并获取版本信息：
   ```bash
   whoami --version
   ```

## 提示
- 使用 `whoami` 命令时，确保你在终端中运行它，以便正确获取当前用户信息。
- 该命令在脚本中也很有用，可以帮助你确认脚本以哪个用户身份运行。