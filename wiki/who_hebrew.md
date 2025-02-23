# [דביאן] Debian Almquist Shell (dash) who: הצגת משתמשים מחוברים

## Overview
הפקודה `who` משמשת להצגת רשימת המשתמשים המחוברים למערכת. היא מציגה מידע כמו שם המשתמש, הטרמינל שבו הם מחוברים, ותאריך ושעת החיבור.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
who [אפשרויות] [ארגומנטים]
```

## Common Options
- `-a`: מציג מידע נוסף על המשתמשים המחוברים, כולל תהליכים פעילים.
- `-b`: מציג את הזמן האחרון שבו המערכת הופעלה מחדש.
- `-q`: מציג את שמות המשתמשים המחוברים ומספרם בלבד.

## Common Examples
- הצגת רשימת המשתמשים המחוברים:
  ```sh
  who
  ```

- הצגת מידע נוסף על המשתמשים:
  ```sh
  who -a
  ```

- הצגת הזמן האחרון שבו המערכת הופעלה מחדש:
  ```sh
  who -b
  ```

- הצגת שמות המשתמשים ומספרם בלבד:
  ```sh
  who -q
  ```

## Tips
- השתמשו בפקודה `who` יחד עם `grep` כדי לחפש משתמשים ספציפיים.
- ניתן לשלב את `who` עם פקודות אחרות כמו `wc -l` כדי לספור את מספר המשתמשים המחוברים:
  ```sh
  who | wc -l
  ```
- זכרו שהפקודה `who` מציגה רק את המשתמשים המחוברים כרגע, ולא את כל המשתמשים במערכת.