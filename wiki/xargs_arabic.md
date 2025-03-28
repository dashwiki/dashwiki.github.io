# [نظام التشغيل] Debian Almquist Shell (dash) xargs الاستخدام: تنفيذ الأوامر مع مدخلات متعددة

## نظرة عامة
يستخدم أمر `xargs` في شل داش (dash) لتحويل المدخلات القياسية إلى وسائط للأوامر. يسمح لك بتشغيل أوامر متعددة باستخدام مخرجات أو مدخلات أخرى، مما يجعله أداة قوية لمعالجة البيانات.

## الاستخدام
الصيغة الأساسية للأمر هي:
```bash
xargs [options] [arguments]
```

## الخيارات الشائعة
- `-n N`: يحدد عدد الوسائط التي يتم تمريرها إلى الأمر في كل مرة.
- `-d DELIMITER`: يحدد الفاصل الذي يستخدم لتقسيم المدخلات.
- `-p`: يطلب تأكيد المستخدم قبل تنفيذ كل أمر.
- `-0`: يتعامل مع المدخلات التي تحتوي على أحرف جديدة (null-terminated).

## أمثلة شائعة
- **تمرير قائمة من الملفات إلى الأمر `rm`:**
```bash
find . -name "*.tmp" | xargs rm
```
هذا الأمر سيبحث عن جميع الملفات ذات الامتداد `.tmp` في الدليل الحالي ويقوم بحذفها.

- **استخدام `xargs` مع `echo`:**
```bash
echo "file1 file2 file3" | xargs -n 1 echo
```
هذا الأمر سيقوم بطباعة كل اسم ملف في سطر جديد.

- **تمرير المدخلات إلى `grep`:**
```bash
cat file.txt | xargs grep "pattern"
```
هذا الأمر سيبحث عن "pattern" في محتويات `file.txt`.

## نصائح
- استخدم الخيار `-n` لتحديد عدد الوسائط التي تريد تمريرها لتجنب تجاوز حدود الأوامر.
- تأكد من استخدام الخيار `-0` عند التعامل مع أسماء الملفات التي قد تحتوي على مسافات أو أحرف خاصة.
- استخدم `-p` لتأكيد الأوامر قبل التنفيذ، خاصة عند إجراء تغييرات كبيرة مثل الحذف.