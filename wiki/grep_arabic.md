# [ديبيان] Debian Almquist Shell (dash) grep الاستخدام: البحث عن النصوص في الملفات

## Overview
أداة `grep` هي أداة قوية تستخدم للبحث عن نصوص معينة داخل الملفات. تقوم هذه الأداة بتمشيط محتويات الملفات وتحديد الأسطر التي تحتوي على النص المطلوب، مما يجعلها مفيدة جدًا في تحليل البيانات والبحث عن المعلومات.

## Usage
الصيغة الأساسية لاستخدام الأمر `grep` هي:

```bash
grep [options] [arguments]
```

## Common Options
- `-i`: تجاهل حالة الأحرف أثناء البحث.
- `-v`: عكس النتائج، أي عرض الأسطر التي لا تحتوي على النص المطلوب.
- `-r`: البحث بشكل متكرر في الدلائل والمجلدات.
- `-n`: عرض أرقام الأسطر التي تحتوي على النص.
- `-l`: عرض أسماء الملفات التي تحتوي على النص فقط.

## Common Examples
- **البحث عن نص داخل ملف:**
  ```bash
  grep "نص" filename.txt
  ```

- **البحث عن نص مع تجاهل حالة الأحرف:**
  ```bash
  grep -i "نص" filename.txt
  ```

- **البحث في جميع الملفات داخل دليل:**
  ```bash
  grep -r "نص" /path/to/directory
  ```

- **عرض الأسطر التي لا تحتوي على النص:**
  ```bash
  grep -v "نص" filename.txt
  ```

- **عرض أرقام الأسطر التي تحتوي على النص:**
  ```bash
  grep -n "نص" filename.txt
  ```

## Tips
- استخدم الخيار `-i` عندما لا تكون متأكدًا من حالة الأحرف في النص.
- إذا كنت تبحث في ملفات كثيرة، استخدم الخيار `-r` لتوفير الوقت.
- يمكنك دمج `grep` مع أوامر أخرى باستخدام الأنابيب (`|`) لتحسين نتائج البحث.