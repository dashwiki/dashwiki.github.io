# [دبیان] Debian Almquist Shell (dash) jobs استفاده: نمایش وظایف در حال اجرا

## Overview
دستور `jobs` در شل دبیان آلکوئیست (dash) برای نمایش لیست وظایف (jobs) در حال اجرا و وضعیت آن‌ها استفاده می‌شود. این دستور به شما کمک می‌کند تا ببینید کدام فرآیندها در پس‌زمینه در حال اجرا هستند و وضعیت آن‌ها چیست.

## Usage
سینتکس پایه دستور به صورت زیر است:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: نمایش شناسه‌های فرآیند (PID) برای هر وظیفه.
- `-n`: فقط وظایف جدید را نمایش می‌دهد.
- `-p`: فقط شناسه‌های فرآیند را نمایش می‌دهد.

## Common Examples
### نمایش وظایف در حال اجرا
برای نمایش تمام وظایف در حال اجرا، کافیست دستور زیر را اجرا کنید:

```bash
jobs
```

### نمایش وظایف با شناسه‌های فرآیند
برای نمایش وظایف همراه با شناسه‌های فرآیند، از گزینه `-l` استفاده کنید:

```bash
jobs -l
```

### نمایش وظایف جدید
اگر فقط می‌خواهید وظایف جدید را ببینید، از گزینه `-n` استفاده کنید:

```bash
jobs -n
```

### نمایش شناسه‌های فرآیند
برای نمایش فقط شناسه‌های فرآیند، از گزینه `-p` استفاده کنید:

```bash
jobs -p
```

## Tips
- از دستور `bg` برای ادامه دادن یک وظیفه در پس‌زمینه استفاده کنید.
- می‌توانید از دستور `fg` برای بازگرداندن یک وظیفه به حالت پیش‌زمینه استفاده کنید.
- برای مدیریت بهتر وظایف، به یاد داشته باشید که می‌توانید از `kill` برای متوقف کردن وظایف استفاده کنید.