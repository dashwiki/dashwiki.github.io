# [ديبيان] Debian Almquist Shell (dash) strace الاستخدام: تتبع استدعاءات النظام

## Overview
أداة `strace` تُستخدم لتتبع استدعاءات النظام التي تقوم بها البرامج. من خلال استخدام `strace`, يمكنك رؤية كيفية تفاعل البرنامج مع نظام التشغيل، مما يساعد في تشخيص الأخطاء وفهم سلوك البرنامج.

## Usage
يمكنك استخدام `strace` مع الصيغة الأساسية التالية:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: يلخص إحصائيات استدعاءات النظام.
- `-e trace=SYSCALL`: يحدد نوع استدعاءات النظام التي تريد تتبعها.
- `-o filename`: يكتب المخرجات إلى ملف بدلاً من الشاشة.
- `-p pid`: يتتبع عملية موجودة بالفعل باستخدام معرف العملية المحدد.

## Common Examples
- لتتبع برنامج `ls`:

```bash
strace ls
```

- لتتبع استدعاءات النظام لعملية موجودة بالفعل:

```bash
strace -p 1234
```

- لتتبع استدعاءات النظام وكتابة المخرجات إلى ملف:

```bash
strace -o output.txt ls
```

- للحصول على ملخص لإحصائيات استدعاءات النظام:

```bash
strace -c ls
```

## Tips
- استخدم الخيار `-o` لتخزين المخرجات في ملف، مما يسهل مراجعتها لاحقًا.
- عند تتبع برامج معقدة، قد يكون من المفيد استخدام `-e trace=network` لتتبع استدعاءات الشبكة فقط.
- تأكد من تشغيل `strace` كمسؤول إذا كنت بحاجة إلى تتبع عمليات تتطلب أذونات مرتفعة.