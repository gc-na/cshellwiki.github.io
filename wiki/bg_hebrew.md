# [לינוקס] C Shell (csh) bg שימוש: העברת תהליך לרקע

## Overview
הפקודה `bg` ב-C Shell (csh) משמשת להעברת תהליך שרץ ברקע, כך שהוא יכול להמשיך לפעול מבלי לחסום את שורת הפקודה. זה שימושי כאשר רוצים להמשיך להשתמש בשורת הפקודה בזמן שתהליך מסוים רץ.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
bg [options] [arguments]
```

## Common Options
- `job_id`: מזהה התהליך שברצונך להעביר לרקע. ניתן להשתמש במזהה התהליך או במספר העבודה (job number).
- `-l`: מציג את מזהי התהליך (PID) של התהליכים ברקע.

## Common Examples
להלן מספר דוגמאות שימושיות:

1. **העברת תהליך לרקע**
   ```csh
   sleep 60 &
   bg %1
   ```
   כאן, התהליך `sleep 60` רץ ברקע, והפקודה `bg %1` מעבירה אותו לרקע אם הוא לא כבר שם.

2. **הצגת תהליכים ברקע**
   ```csh
   jobs
   ```
   פקודה זו מציגה את כל התהליכים שרצים ברקע.

3. **החזרת תהליך לרקע**
   ```csh
   bg %2
   ```
   כאן, התהליך השני ברשימה מועבר לרקע.

## Tips
- השתמש בפקודת `jobs` כדי לבדוק אילו תהליכים רצים ברקע.
- אם אתה רוצה להפסיק תהליך לפני העברתו לרקע, השתמש בפקודת `Ctrl+Z` כדי להפסיק אותו ואז השתמש ב-`bg`.
- זכור כי תהליכים ברקע לא יכולים לקבל קלט מהמשתמש, אז ודא שהם לא זקוקים לו.