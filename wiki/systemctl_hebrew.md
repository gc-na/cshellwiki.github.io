# [לינוקס] Bash systemctl שימוש: ניהול שירותים במערכת

## Overview
הפקודה `systemctl` היא כלי ניהול מרכזי במערכות לינוקס המשתמשות ב-systemd. היא מאפשרת למשתמשים לנהל שירותים, לבדוק את מצבם, להפעיל ולהפסיק אותם, ולבצע פעולות נוספות הקשורות לניהול מערכת.

## Usage
התחביר הבסיסי של הפקודה הוא:

```bash
systemctl [options] [arguments]
```

## Common Options
- `start`: מפעיל שירות.
- `stop`: מפסיק שירות.
- `restart`: מפעיל מחדש שירות.
- `status`: מציג את מצב השירות.
- `enable`: מפעיל את השירות באופן אוטומטי בעת אתחול המערכת.
- `disable`: מונע מהשירות לפעול באופן אוטומטי בעת אתחול המערכת.

## Common Examples
- הפעלת שירות:
  ```bash
  systemctl start apache2
  ```

- הפסקת שירות:
  ```bash
  systemctl stop apache2
  ```

- הפעלת מחדש של שירות:
  ```bash
  systemctl restart apache2
  ```

- בדיקת מצב של שירות:
  ```bash
  systemctl status apache2
  ```

- הפעלת שירות אוטומטית בעת אתחול:
  ```bash
  systemctl enable apache2
  ```

- מניעת שירות אוטומטית בעת אתחול:
  ```bash
  systemctl disable apache2
  ```

## Tips
- תמיד בדוק את מצב השירות לאחר ביצוע פעולות עם `systemctl status`.
- השתמש בפקודה `journalctl` כדי לבדוק את הלוגים של השירותים במידת הצורך.
- זכור להריץ פקודות `systemctl` עם הרשאות מנהל (sudo) כאשר זה נדרש.