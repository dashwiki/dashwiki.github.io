# [ديبيان] Debian Almquist Shell (dash) dstat الاستخدام: عرض إحصائيات النظام في الوقت الحقيقي

## Overview
يُستخدم أمر `dstat` لعرض إحصائيات النظام في الوقت الحقيقي، مما يسمح للمستخدمين بمراقبة أداء النظام بشكل شامل. يجمع `dstat` بين ميزات أدوات مثل `vmstat` و`iostat` و`netstat`، مما يوفر معلومات حول استخدام المعالج، الذاكرة، الشبكة، والقرص.

## Usage
يمكن استخدام الأمر `dstat` مع خيارات مختلفة لتخصيص المعلومات المعروضة. الصيغة الأساسية هي:

```bash
dstat [options] [arguments]
```

## Common Options
- `-c`: عرض استخدام وحدة المعالجة المركزية.
- `-d`: عرض إحصائيات القرص.
- `-n`: عرض إحصائيات الشبكة.
- `-m`: عرض إحصائيات الذاكرة.
- `--time`: عرض الوقت الحالي مع الإحصائيات.

## Common Examples
إليك بعض الأمثلة العملية لاستخدام `dstat`:

1. **عرض استخدام وحدة المعالجة المركزية والذاكرة:**
   ```bash
   dstat -c -m
   ```

2. **عرض إحصائيات الشبكة والقرص:**
   ```bash
   dstat -n -d
   ```

3. **عرض جميع الإحصائيات مع الوقت:**
   ```bash
   dstat --time -cdmn
   ```

4. **تسجيل الإحصائيات إلى ملف:**
   ```bash
   dstat -cdmn --output output.csv
   ```

## Tips
- استخدم `dstat` مع الخيارات المناسبة لمراقبة الجوانب التي تهمك أكثر.
- يمكنك دمج عدة خيارات للحصول على رؤية شاملة لأداء النظام.
- إذا كنت بحاجة إلى تحليل البيانات لاحقًا، استخدم خيار `--output` لتخزين النتائج في ملف.