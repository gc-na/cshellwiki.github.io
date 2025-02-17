# [לינוקס] Bash getopts שימוש: [ניתוב אפשרויות בפקודות]

## Overview
הפקודה `getopts` ב-Bash משמשת לניהול אפשרויות ופרמטרים בפקודות. היא מאפשרת למפתחים לנתח את הפרמטרים שנמסרו לסקריפט בצורה נוחה ומסודרת, כך שניתן יהיה להגיב בהתאם לאופציות שנבחרו.

## Usage
התחביר הבסיסי של הפקודה הוא:

```bash
getopts [options] [arguments]
```

## Common Options
- `-a`: מאפשר להגדיר אפשרויות נוספות.
- `-b`: משמש לאופציות בוליאניות.
- `-c`: מאפשר לספור את מספר הפעמים שהאופציה הופיעה.
- `-d`: מדפיס מידע נוסף על האופציות.

## Common Examples

### דוגמה 1: שימוש בסיסי ב-getopts
```bash
#!/bin/bash

while getopts "a:b:c:" opt; do
  case $opt in
    a) echo "Option A: $OPTARG" ;;
    b) echo "Option B: $OPTARG" ;;
    c) echo "Option C: $OPTARG" ;;
    *) echo "Invalid option" ;;
  esac
done
```

### דוגמה 2: אופציה בוליאנית
```bash
#!/bin/bash

while getopts "ab" opt; do
  case $opt in
    a) echo "Option A is set" ;;
    b) echo "Option B is set" ;;
    *) echo "Invalid option" ;;
  esac
done
```

### דוגמה 3: ספירת אופציות
```bash
#!/bin/bash

count=0
while getopts "a" opt; do
  ((count++))
done
echo "Option A was provided $count times."
```

## Tips
- תמיד השתמשו ב-`case` כדי לנתח את האופציות, זה מקנה קוד ברור ומסודר.
- כדאי להוסיף טיפול באופציות לא חוקיות כדי לשפר את חוויית המשתמש.
- השתמשו ב-`OPTARG` כדי לגשת לערך של האופציה שנבחרה, זה מאפשר גמישות רבה יותר.