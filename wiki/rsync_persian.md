# [سیستم‌عامل] Debian Almquist Shell (dash) rsync استفاده: [همگام‌سازی فایل‌ها]

## Overview
دستور `rsync` ابزاری قدرتمند برای همگام‌سازی و انتقال فایل‌ها و دایرکتوری‌ها بین سیستم‌ها یا درون یک سیستم است. این دستور به شما امکان می‌دهد تا فایل‌ها را به صورت محلی یا از طریق شبکه منتقل کنید و تنها تغییرات را ارسال کنید، که این امر باعث صرفه‌جویی در زمان و پهنای باند می‌شود.

## Usage
سینتکس پایه دستور `rsync` به صورت زیر است:

```bash
rsync [options] [arguments]
```

## Common Options
- `-a`: حالت آرشیو، شامل کپی کردن فایل‌ها به صورت بازگشتی و حفظ مجوزها و زمان‌ها.
- `-v`: نمایش جزئیات بیشتر در حین انتقال (verbose).
- `-z`: فشرده‌سازی داده‌ها در حین انتقال.
- `-r`: کپی کردن دایرکتوری‌ها به صورت بازگشتی.
- `--delete`: حذف فایل‌های مقصد که در مبدا وجود ندارند.

## Common Examples
### همگام‌سازی یک دایرکتوری محلی
```bash
rsync -av /path/to/source/ /path/to/destination/
```

### همگام‌سازی با سرور از راه دور
```bash
rsync -avz /local/path user@remote:/remote/path
```

### همگام‌سازی و حذف فایل‌های اضافی
```bash
rsync -av --delete /path/to/source/ /path/to/destination/
```

### همگام‌سازی با فشرده‌سازی
```bash
rsync -avz /local/path user@remote:/remote/path
```

## Tips
- همیشه از گزینه `-n` (dry run) استفاده کنید تا ببینید چه فایل‌هایی منتقل خواهند شد بدون اینکه تغییر واقعی ایجاد شود.
- برای انتقال فایل‌های بزرگ، از گزینه `--progress` استفاده کنید تا پیشرفت انتقال را مشاهده کنید.
- در صورت نیاز به همگام‌سازی با سرورهای SSH، می‌توانید از گزینه `-e ssh` استفاده کنید.