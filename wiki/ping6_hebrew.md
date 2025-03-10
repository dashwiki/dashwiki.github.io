# [לינוקס] Debian Almquist Shell (dash) ping6 שימוש: בדיקת חיבוריות IPv6

## Overview
הפקודה `ping6` משמשת לבדוק חיבוריות לרשת עבור כתובות IPv6. היא שולחת מנות נתונים לכתובת היעד ומודדת את הזמן שלוקח לקבל תגובה, מה שמסייע בזיהוי בעיות ברשת.

## Usage
התחביר הבסיסי של הפקודה הוא:

```bash
ping6 [אפשרויות] [כתובת יעד]
```

## Common Options
- `-c <מספר>`: קובע את מספר המנות שיש לשלוח.
- `-i <שניות>`: קובע את הזמן בין שליחת מנות (בברירת מחדל 1 שניה).
- `-w <שניות>`: קובע את הזמן המקסימלי לחכות לתגובות לפני סיום הפקודה.

## Common Examples
1. לשלוח 4 מנות לכתובת IPv6:
   ```bash
   ping6 -c 4 2001:0db8:85a3:0000:0000:8a2e:0370:7334
   ```

2. לבדוק חיבוריות לשרת עם זמן המתנה של 2 שניות בין המנות:
   ```bash
   ping6 -i 2 2001:0db8:85a3:0000:0000:8a2e:0370:7334
   ```

3. להפסיק את הפקודה לאחר 10 שניות:
   ```bash
   ping6 -w 10 2001:0db8:85a3:0000:0000:8a2e:0370:7334
   ```

## Tips
- השתמשו באפשרות `-c` כדי לשלוח מספר מוגבל של מנות, מה שיכול לחסוך בזמן.
- אם אתם מתמודדים עם בעיות חיבור, בדקו את הכתובת היעד והוודאו שהיא נכונה.
- ניתן להשתמש בפקודה `ping6` כדי לבדוק חיבוריות בין מחשבים ברשת מקומית או באינטרנט.