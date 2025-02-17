# [לינוקס] Bash helm שימוש: ניהול חבילות Kubernetes

## Overview
הפקודה `helm` משמשת ככלי לניהול חבילות עבור Kubernetes. היא מאפשרת למפתחים ולמפעילים להתקין, לעדכן ולנהל יישומים על גבי קלאסטרים של Kubernetes בצורה קלה ויעילה.

## Usage
הסינטקס הבסיסי של הפקודה הוא:
```
helm [options] [arguments]
```

## Common Options
- `install`: מתקין חבילה חדשה.
- `upgrade`: מעדכן חבילה קיימת לגרסה חדשה.
- `rollback`: מחזיר חבילה לגרסה קודמת.
- `uninstall`: מסיר חבילה מהקלאסטר.
- `list`: מציג את כל החבילות המותקנות בקלאסטר.

## Common Examples
### התקנת חבילה חדשה
```bash
helm install my-release stable/nginx
```

### עדכון חבילה
```bash
helm upgrade my-release stable/nginx
```

### החזרת חבילה לגרסה קודמת
```bash
helm rollback my-release 1
```

### הסרת חבילה
```bash
helm uninstall my-release
```

### הצגת רשימת חבילות מותקנות
```bash
helm list
```

## Tips
- תמיד בדוק את הגרסאות הזמינות של החבילות לפני ההתקנה או העדכון.
- השתמש בפקודת `helm repo update` כדי לוודא שיש לך את המידע העדכני על החבילות.
- שקול להשתמש בגרסאות מתויגות של חבילות כדי למנוע בעיות עם עדכונים לא צפויים.