# [לינוקס] Bash while שימוש: חזרה על פקודות עד שהתנאי לא מתקיים

## Overview
הפקודה `while` ב-Bash משמשת להרצת בלוק של פקודות כל עוד התנאי שניתן להן מתקיים. זהו כלי יעיל לביצוע חזרות על פקודות עד שהמצב משתנה.

## Usage
התחביר הבסיסי של הפקודה `while` הוא:

```bash
while [תנאי]
do
    פקודות
done
```

## Common Options
- אין אפשרויות מיוחדות לפקודת `while`, אך ניתן לשלב אותה עם פקודות אחרות כמו `break` ו-`continue` לשליטה על הלולאה.

## Common Examples

### דוגמה 1: חזרה עד שהמשתנה קטן מ-5
```bash
count=0
while [ $count -lt 5 ]
do
    echo "Count is $count"
    ((count++))
done
```

### דוגמה 2: קריאת קלט מהמשתמש
```bash
input=""
while [ "$input" != "exit" ]
do
    read -p "Enter something (type 'exit' to quit): " input
    echo "You entered: $input"
done
```

### דוגמה 3: חזרה על קבצים בתיקייה
```bash
for file in *.txt
do
    while read line
    do
        echo "$line"
    done < "$file"
done
```

## Tips
- השתמש ב-`break` כדי לצאת מהלולאה בתנאים מסוימים.
- השתמש ב-`continue` כדי לדלג על חזרה מסוימת בלולאה.
- הקפד על סגירת הלולאה עם `done` כדי למנוע שגיאות סינטקס.