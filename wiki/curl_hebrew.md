# [לינוקס] Bash curl שימוש: שליחת בקשות HTTP

## Overview
הפקודה `curl` משמשת לשליחת בקשות HTTP ו-HTTPS, והיא מאפשרת למשתמשים לתקשר עם שרתים דרך פרוטוקולים שונים. בעזרת `curl`, ניתן להוריד קבצים, לשלוח נתונים, ולבצע בדיקות על שירותים שונים באינטרנט.

## Usage
התחביר הבסיסי של הפקודה הוא:

```bash
curl [אפשרויות] [ארגומנטים]
```

## Common Options
- `-X`: קובע את סוג הבקשה (GET, POST, PUT וכו').
- `-d`: שולח נתונים בגוף הבקשה.
- `-H`: מוסיף כותרות לבקשה.
- `-o`: שומר את התגובה לקובץ.
- `-I`: מבקש רק את הכותרות של התגובה.

## Common Examples
1. **שליחת בקשת GET:**
   ```bash
   curl https://www.example.com
   ```

2. **שליחת בקשת POST עם נתונים:**
   ```bash
   curl -X POST -d "name=John&age=30" https://www.example.com/api
   ```

3. **שימוש בכותרת מותאמת אישית:**
   ```bash
   curl -H "Authorization: Bearer TOKEN" https://www.example.com/protected
   ```

4. **שמור את התגובה לקובץ:**
   ```bash
   curl -o response.txt https://www.example.com
   ```

5. **בקשת כותרות בלבד:**
   ```bash
   curl -I https://www.example.com
   ```

## Tips
- השתמשו באופציה `-v` כדי לראות את פרטי הבקשה והתגובה, זה יכול לעזור בפתרון בעיות.
- אם אתם עובדים עם API, כדאי לבדוק את התיעוד של ה-API כדי לדעת אילו כותרות ונתונים יש לשלוח.
- זכרו להשתמש באופציה `-L` כדי לעקוב אחרי הפניות (redirects) אוטומטית.