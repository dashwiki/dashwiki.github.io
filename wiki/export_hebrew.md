# [דביאן] Debian Almquist Shell (dash) export שימוש: הגדרת משתנים בסביבת העבודה

## Overview
הפקודה `export` משמשת בהגדרת משתנים בסביבת העבודה של ה-shell. כאשר משתנה מיוצא, הוא זמין לכל התהליכים שיתחילו מה-shell הנוכחי.

## Usage
התחביר הבסיסי של הפקודה הוא:

```sh
export [options] [arguments]
```

## Common Options
- `-p`: מציג את כל המשתנים המיוצאים בסביבת העבודה הנוכחית.
- `VAR=value`: מגדיר משתנה חדש או מעדכן משתנה קיים ומייצא אותו.

## Common Examples
- לייצא משתנה חדש בשם `MY_VAR` עם ערך `hello`:

```sh
export MY_VAR=hello
```

- לבדוק אם המשתנה ייצא בהצלחה:

```sh
echo $MY_VAR
```

- לייצא משתנה קיים בשם `PATH` עם ערך נוסף:

```sh
export PATH=$PATH:/new/directory
```

- להציג את כל המשתנים המיוצאים:

```sh
export -p
```

## Tips
- תמיד כדאי לבדוק את ערך המשתנים המיוצאים בעזרת `echo` כדי לוודא שההגדרות נכונות.
- זכרו שברגע שמייצאים משתנה, הוא יהיה זמין לכל התהליכים שיתחילו מה-shell הנוכחי, לכן יש להשתמש בזהירות עם שמות משתנים כדי למנוע התנגשויות.