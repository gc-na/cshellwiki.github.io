# [לינוקס] Bash sftp שימוש: העברת קבצים בצורה מאובטחת

## Overview
הפקודה `sftp` (Secure File Transfer Protocol) משמשת להעברת קבצים בין מחשבים בצורה מאובטחת באמצעות SSH. היא מאפשרת למשתמשים להתחבר לשרתים מרוחקים ולהעביר קבצים בקלות ובבטחה.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
sftp [options] [arguments]
```

## Common Options
- `-o` : מאפשר להגדיר אפשרויות חיבור נוספות.
- `-P` : מציין את מספר הפורט לשימוש (ברירת מחדל היא 22).
- `-v` : מצב מפורט, מציג מידע נוסף על תהליך החיבור וההעברה.

## Common Examples
- להתחבר לשרת SFTP:
```bash
sftp user@hostname
```

- להוריד קובץ מהשרת:
```bash
sftp user@hostname:/path/to/remote/file /path/to/local/destination
```

- להעלות קובץ לשרת:
```bash
sftp /path/to/local/file user@hostname:/path/to/remote/destination
```

- להציג את התוכן של תיקייה מרוחקת:
```bash
sftp user@hostname
ls /path/to/remote/directory
```

## Tips
- השתמש באופציה `-v` כדי לאבחן בעיות חיבור.
- תמיד ודא שאתה מחובר לרשת מאובטחת לפני העברת קבצים רגישים.
- שקול להשתמש במפתחות SSH במקום סיסמאות לשיפור האבטחה.