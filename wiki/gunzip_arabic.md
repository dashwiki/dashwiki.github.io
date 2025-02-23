# [ديبيان] Debian Almquist Shell (dash) gunzip الاستخدام: فك ضغط الملفات

## Overview
يستخدم الأمر `gunzip` لفك ضغط الملفات المضغوطة بتنسيق Gzip. يقوم هذا الأمر بإزالة الضغط عن الملفات، مما يجعل البيانات الأصلية متاحة للاستخدام.

## Usage
تكون الصيغة الأساسية للأمر كالتالي:

```bash
gunzip [options] [arguments]
```

## Common Options
- `-c`: يخرج البيانات إلى المعيار القياسي (stdout) بدلاً من الكتابة إلى ملف.
- `-f`: يفرض فك الضغط حتى إذا كان الملف الناتج موجودًا بالفعل.
- `-k`: يحتفظ بالملف المضغوط الأصلي بعد فك الضغط.
- `-r`: يقوم بفك ضغط الملفات في الدلائل الفرعية بشكل متكرر.

## Common Examples
- لفك ضغط ملف مضغوط:
  ```bash
  gunzip file.txt.gz
  ```

- لفك ضغط ملف مع الاحتفاظ بالملف الأصلي:
  ```bash
  gunzip -k file.txt.gz
  ```

- لفك ضغط جميع الملفات المضغوطة في الدليل الحالي:
  ```bash
  gunzip *.gz
  ```

- لفك ضغط ملف وإخراج البيانات إلى المعيار القياسي:
  ```bash
  gunzip -c file.txt.gz > output.txt
  ```

## Tips
- تأكد من أن لديك مساحة كافية على القرص قبل فك ضغط الملفات الكبيرة.
- استخدم الخيار `-k` إذا كنت ترغب في الاحتفاظ بالنسخة المضغوطة الأصلية.
- يمكنك دمج `gunzip` مع أوامر أخرى باستخدام أنابيب (pipes) لتحسين سير العمل.