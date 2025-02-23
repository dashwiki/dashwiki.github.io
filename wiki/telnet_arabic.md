# [ديبيان] Debian Almquist Shell (dash) telnet الاستخدام: الاتصال بخادم بعيد

## نظرة عامة
يستخدم أمر telnet لإنشاء اتصال مع خادم بعيد عبر بروتوكول TCP/IP. يتيح لك هذا الأمر التفاعل مع الخادم عن بُعد، مما يجعله مفيدًا للاختبار واستكشاف الأخطاء وإصلاحها.

## الاستخدام
الصيغة الأساسية للأمر هي:

```bash
telnet [options] [arguments]
```

## الخيارات الشائعة
- `-l username`: لتسجيل الدخول باسم مستخدم محدد.
- `-d`: لتفعيل وضع التصحيح.
- `-n`: لتحديد ملف السجل.
- `-h`: لعرض معلومات المساعدة.

## أمثلة شائعة
- الاتصال بخادم عبر عنوان IP:
    ```bash
    telnet 192.168.1.1
    ```

- الاتصال بخادم باستخدام اسم المضيف:
    ```bash
    telnet example.com
    ```

- تسجيل الدخول باسم مستخدم محدد:
    ```bash
    telnet -l user example.com
    ```

- استخدام وضع التصحيح:
    ```bash
    telnet -d example.com
    ```

## نصائح
- تأكد من أن الخادم الذي تتصل به يدعم بروتوكول telnet.
- استخدم telnet فقط في الشبكات الموثوقة، حيث أن البيانات تُرسل بدون تشفير.
- يمكنك استخدام telnet لاختبار المنافذ المفتوحة على الخادم باستخدام الأمر `telnet [hostname] [port]`.