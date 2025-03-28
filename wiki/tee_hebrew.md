# [דביאן] Debian Almquist Shell (dash) tee שימוש: העתקת פלט לקבצים

## Overview
הפקודה `tee` משמשת להעתקת פלט מפקודה אחת לקובץ או יותר, תוך כדי הצגת הפלט במסך. זה מאפשר למשתמש לראות את הפלט בזמן שהוא שומר אותו לקובץ.

## Usage
התחביר הבסיסי של הפקודה הוא:
```bash
tee [אפשרויות] [ארגומנטים]
```

## Common Options
- `-a` או `--append`: מוסיף את הפלט לקובץ קיים במקום להחליף אותו.
- `-i` או `--ignore-interrupts`: מתעלם מהפרעות (interrupts).
- `-p` או `--output-error`: קובע כיצד לטפל בשגיאות פלט.

## Common Examples
1. **שימוש בסיסי**: העתקת פלט לקובץ.
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. **הוספת פלט לקובץ קיים**:
   ```bash
   echo "Another line" | tee -a output.txt
   ```

3. **העתקת פלט לשני קבצים**:
   ```bash
   echo "Hello again!" | tee file1.txt file2.txt
   ```

4. **שימוש עם פקודות אחרות**: לדוגמה, העברת פלט של `ls` לקובץ.
   ```bash
   ls -l | tee directory_list.txt
   ```

## Tips
- השתמש באופציה `-a` כאשר אתה רוצה לשמור פלט לקובץ מבלי לאבד נתונים קיימים.
- ניתן לשלב את `tee` עם פקודות אחרות בשרשרת (pipeline) כדי לשמור פלט בכל שלב.
- זכור לבדוק את הרשאות הגישה לקבצים כדי למנוע שגיאות בעת השמירה.