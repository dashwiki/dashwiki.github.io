# [דביאן] Debian Almquist Shell (dash) comm: השוואת קבצים

## Overview
הפקודה `comm` משווה בין שני קבצים טקסטואליים ומציגה את השורות הייחודיות והמשותפות להם. היא שימושית במיוחד כאשר רוצים לראות את ההבדלים בין שני קבצים או רשימות.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
comm [אפשרויות] [ארגומנטים]
```

## Common Options
- `-1`: לא להציג שורות שמופיעות רק בקובץ הראשון.
- `-2`: לא להציג שורות שמופיעות רק בקובץ השני.
- `-3`: לא להציג שורות שמופיעות בשני הקבצים.
- `-i`: להתעלם מהבדלי רישיות בעת ההשוואה.

## Common Examples
להלן מספר דוגמאות שימושיות:

1. השוואת שני קבצים והצגת כל השורות:
   ```bash
   comm file1.txt file2.txt
   ```

2. הצגת שורות שמופיעות רק בקובץ הראשון:
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. הצגת שורות שמופיעות רק בקובץ השני:
   ```bash
   comm -23 file1.txt file2.txt
   ```

4. השוואה תוך התעלמות מהבדלי רישיות:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- ודאו שהקבצים ממוינים לפני השימוש ב-`comm`, אחרת התוצאות לא יהיו מדויקות.
- ניתן לשלב את `comm` עם פקודות אחרות כמו `sort` כדי למיין קבצים לפני ההשוואה:
  ```bash
  comm <(sort file1.txt) <(sort file2.txt)
  ```
- השתמשו באפשרויות השונות כדי להתאים את הפלט לצרכים שלכם, כך שתוכלו להתמקד במידע החשוב ביותר.