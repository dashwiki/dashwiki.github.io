# [لینوکس] Debian Almquist Shell (dash) telnet استفاده: ارتباط با سرورهای شبکه

## Overview
دستور `telnet` یک ابزار خط فرمان است که به کاربران اجازه می‌دهد تا به سرورهای شبکه متصل شوند و با استفاده از پروتکل Telnet ارتباط برقرار کنند. این دستور معمولاً برای عیب‌یابی و مدیریت سرورها استفاده می‌شود.

## Usage
سینتکس پایه دستور `telnet` به صورت زیر است:

```bash
telnet [options] [arguments]
```

## Common Options
- `-l username`: برای ورود به سیستم با نام کاربری مشخص.
- `-d`: فعال‌سازی حالت عیب‌یابی.
- `-n`: غیرفعال کردن نوار وضعیت.
- `-h`: نمایش راهنما و گزینه‌های موجود.

## Common Examples
### اتصال به یک سرور
برای اتصال به یک سرور خاص، می‌توانید از دستور زیر استفاده کنید:

```bash
telnet example.com 80
```

### ورود با نام کاربری مشخص
برای ورود به یک سرور با نام کاربری خاص، از گزینه `-l` استفاده کنید:

```bash
telnet -l myuser example.com
```

### عیب‌یابی اتصال
برای فعال‌سازی حالت عیب‌یابی، می‌توانید از گزینه `-d` استفاده کنید:

```bash
telnet -d example.com 23
```

## Tips
- از `telnet` برای بررسی پورت‌های باز و ارتباطات شبکه استفاده کنید.
- توجه داشته باشید که Telnet اطلاعات را به صورت متن ساده ارسال می‌کند، بنابراین برای ارتباطات حساس از پروتکل‌های امن‌تری مانند SSH استفاده کنید.
- در صورت عدم نیاز به اتصال، از دستور `quit` برای خروج از جلسه Telnet استفاده کنید.