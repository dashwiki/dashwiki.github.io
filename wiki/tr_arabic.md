# [ديبيان] Debian Almquist Shell (dash) tr <استخدام مكافئ بالعربية>: تحويل الأحرف

## نظرة عامة
أمر `tr` هو أداة تستخدم لتحويل أو حذف الأحرف في النصوص. يمكن استخدامه لتغيير الأحرف الكبيرة إلى صغيرة، أو العكس، أو حتى لاستبدال مجموعة من الأحرف بأخرى.

## الاستخدام
الصيغة الأساسية للأمر هي:

```bash
tr [خيارات] [وسائط]
```

## الخيارات الشائعة
- `-d`: حذف الأحرف المحددة.
- `-s`: ضغط الأحرف المتكررة إلى حرف واحد.
- `-c`: استخدام الأحرف غير المحددة بدلاً من المحددة.

## أمثلة شائعة
- لتحويل الأحرف الصغيرة إلى أحرف كبيرة:

```bash
echo "hello world" | tr 'a-z' 'A-Z'
```

- لحذف جميع الأرقام من النص:

```bash
echo "abc123def456" | tr -d '0-9'
```

- لضغط الأحرف المتكررة إلى حرف واحد:

```bash
echo "aaabbbccc" | tr -s 'a' 'b'
```

- لاستبدال الأحرف:

```bash
echo "apple" | tr 'aeiou' 'AEIOU'
```

## نصائح
- تأكد من استخدام علامات الاقتباس حول الأحرف لتجنب أي مشاكل في التفسير.
- يمكنك دمج `tr` مع أوامر أخرى مثل `grep` أو `sed` لعمليات معالجة نصوص أكثر تعقيدًا.
- استخدم الخيار `-c` بحذر، لأنه سيؤدي إلى استبدال الأحرف غير المحددة فقط.