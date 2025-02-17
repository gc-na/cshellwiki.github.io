# [לינוקס] Bash lvm שימוש: ניהול לוגיים של מחיצות

## Overview
הפקודה `lvm` (Logical Volume Manager) משמשת לניהול מחיצות לוגיות במערכות לינוקס. היא מאפשרת למשתמשים ליצור, למחוק ולנהל מחיצות בצורה גמישה, מה שמקל על ניהול שטח האחסון במערכת.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
lvm [options] [arguments]
```

## Common Options
- `create`: ליצור מחיצה לוגית חדשה.
- `remove`: למחוק מחיצה לוגית קיימת.
- `extend`: להרחיב מחיצה לוגית.
- `reduce`: לצמצם מחיצה לוגית.
- `lvdisplay`: להציג מידע על מחיצות לוגיות.

## Common Examples
1. **יצירת מחיצה לוגית חדשה**:
   ```bash
   lvm lvcreate -n my_volume -L 10G my_volume_group
   ```

2. **הצגת מחיצות לוגיות**:
   ```bash
   lvm lvdisplay
   ```

3. **הרחבת מחיצה לוגית**:
   ```bash
   lvm lvextend -L +5G /dev/my_volume_group/my_volume
   ```

4. **צמצום מחיצה לוגית**:
   ```bash
   lvm lvreduce -L -5G /dev/my_volume_group/my_volume
   ```

5. **מחיקת מחיצה לוגית**:
   ```bash
   lvm lvremove /dev/my_volume_group/my_volume
   ```

## Tips
- תמיד גבה את הנתונים לפני ביצוע שינויים משמעותיים במחיצות.
- השתמש בפקודת `lvdisplay` כדי לבדוק את מצב המחיצות לפני ואחרי ביצוע שינויים.
- הקפד לבדוק את השטח הפנוי במערכת לפני הרחבת מחיצה לוגית.