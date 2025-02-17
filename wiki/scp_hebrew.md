# [לינוקס] Bash scp שימוש: העברת קבצים בין מחשבים

## Overview
הפקודה `scp` (Secure Copy Protocol) משמשת להעברת קבצים בצורה מאובטחת בין מחשבים ברשת. היא משתמשת בפרוטוקול SSH כדי להבטיח שהמידע מועבר בצורה מוצפנת.

## Usage
הסינטקס הבסיסי של הפקודה הוא:

```bash
scp [אפשרויות] [מקור] [יעד]
```

## Common Options
- `-r`: מעביר תיקיות באופן ריקורסיבי.
- `-P`: מציין את מספר הפורט לשימוש (שימו לב שהאות היא גדולה).
- `-i`: מציין את קובץ המפתח הפרטי לשימוש באימות.
- `-v`: מציג מידע מפורט על תהליך ההעברה (מצב verbose).

## Common Examples
1. העברת קובץ מקומי לשרת מרוחק:
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. העברת קובץ משרת מרוחק למחשב מקומי:
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. העברת תיקייה שלמה לשרת מרוחק:
   ```bash
   scp -r /path/to/local/directory user@remote_host:/path/to/remote/directory/
   ```

4. העברת קובץ תוך שימוש במפתח פרטי:
   ```bash
   scp -i /path/to/private_key.pem /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tips
- תמיד השתמשו באפשרות `-v` כדי לקבל מידע נוסף על תהליך ההעברה במקרה של בעיות.
- אם אתם מעבירים קבצים גדולים, שקלו להשתמש באפשרות `-C` לדחיסת הקבצים במהלך ההעברה.
- ודאו שהקבצים שאתם מעבירים מוגנים על ידי שימוש בפרוטוקול SSH.