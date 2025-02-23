# [نظام التشغيل] Debian Almquist Shell (dash) mkdir الاستخدام: إنشاء أدلة جديدة

## Overview
يستخدم الأمر `mkdir` لإنشاء أدلة جديدة في نظام الملفات. يمكن للمستخدمين إنشاء دليل واحد أو أكثر في وقت واحد، مما يسهل تنظيم الملفات والمجلدات.

## Usage
تكون الصيغة الأساسية للأمر كما يلي:

```bash
mkdir [options] [arguments]
```

## Common Options
- `-p`: إنشاء الدلائل الأبوية المطلوبة إذا لم تكن موجودة.
- `-m`: تعيين أذونات الدليل عند إنشائه.
- `--help`: عرض معلومات المساعدة حول الأمر.

## Common Examples
- لإنشاء دليل جديد باسم "myfolder":
```bash
mkdir myfolder
```

- لإنشاء عدة دلائل في وقت واحد:
```bash
mkdir folder1 folder2 folder3
```

- لإنشاء دليل مع الدلائل الأبوية المطلوبة:
```bash
mkdir -p /path/to/new/directory
```

- لإنشاء دليل مع أذونات محددة:
```bash
mkdir -m 755 myfolder
```

## Tips
- استخدم الخيار `-p` لتجنب الأخطاء عند إنشاء دلائل متعددة المستويات.
- تحقق من الأذونات بعد إنشاء الدليل لضمان الوصول الصحيح.
- استخدم أسماء واضحة للدلائل لتسهيل التنظيم والبحث.