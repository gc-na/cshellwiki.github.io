# [לינוקס] Bash endif שימוש: לסיים תנאים

## Overview
הפקודה `endif` משמשת לסיום בלוקי תנאים ב-Bash. היא לא פקודה עצמאית, אלא חלק מהתחביר של פקודות תנאי כמו `if`. כאשר אתה משתמש בפקודת `if`, אתה צריך לסיים את הבלוק שלה עם `endif`.

## Usage
התחביר הבסיסי של הפקודה הוא:
```bash
endif
```

## Common Options
אין אפשרויות נוספות ל`endif`, מכיוון שהיא פקודת סיום בלבד. היא משמשת יחד עם פקודות תנאי אחרות.

## Common Examples
### דוגמה 1: שימוש ב-if עם endif
```bash
if [ "$USER" == "admin" ]; then
    echo "Welcome, admin!"
endif
```

### דוגמה 2: שימוש ב-if עם elseif ו-endif
```bash
if [ "$AGE" -lt 18 ]; then
    echo "You are a minor."
elseif [ "$AGE" -lt 65 ]; then
    echo "You are an adult."
endif
```

### דוגמה 3: שימוש ב-if עם else ו-endif
```bash
if [ -f "file.txt" ]; then
    echo "File exists."
else
    echo "File does not exist."
endif
```

## Tips
- תמיד ודא שיש לך `endif` בסוף בלוק ה-if שלך כדי למנוע שגיאות תחביר.
- השתמש בפקודות תנאי בצורה ברורה כדי לשמור על קריאות הקוד שלך.
- מומלץ להשתמש בפקודות `elif` ו-`else` כדי לייעל את הלוגיקה שלך.