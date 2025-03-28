# [ديبيان] Debian Almquist Shell (dash) uniq الاستخدام: إزالة التكرارات من البيانات

## Overview
يستخدم الأمر `uniq` في نظام التشغيل لينكس لإزالة التكرارات من البيانات. يقوم هذا الأمر بقراءة البيانات من ملف أو من الإدخال القياسي، ويقوم بإخراج الأسطر الفريدة فقط.

## Usage
يمكن استخدام الأمر `uniq` بالشكل التالي:

```bash
uniq [options] [arguments]
```

## Common Options
- `-c`: يقوم بحساب عدد مرات ظهور كل سطر.
- `-d`: يعرض فقط الأسطر المتكررة.
- `-u`: يعرض فقط الأسطر الفريدة.
- `-i`: يتجاهل حالة الأحرف عند مقارنة الأسطر.

## Common Examples
إليك بعض الأمثلة العملية لاستخدام الأمر `uniq`:

1. إزالة التكرارات من ملف نصي:
   ```bash
   uniq input.txt output.txt
   ```

2. عرض الأسطر المتكررة فقط:
   ```bash
   uniq -d input.txt
   ```

3. حساب عدد مرات ظهور كل سطر:
   ```bash
   uniq -c input.txt
   ```

4. تجاهل حالة الأحرف:
   ```bash
   uniq -i input.txt output.txt
   ```

## Tips
- تأكد من فرز البيانات باستخدام الأمر `sort` قبل استخدام `uniq` للحصول على نتائج دقيقة.
- يمكنك استخدام `uniq` مع أنابيب الأوامر لتصفية البيانات في الوقت الحقيقي.
- استخدم الخيار `-u` إذا كنت مهتمًا فقط بالأسطر الفريدة دون التكرارات.