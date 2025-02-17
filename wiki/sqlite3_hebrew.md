# [לינוקס] Bash sqlite3 שימוש: ניהול מסדי נתונים

## Overview
הפקודה `sqlite3` משמשת לניהול מסדי נתונים SQLite. היא מאפשרת למשתמשים ליצור, לערוך ולשאול נתונים מתוך מסדי נתונים בצורה פשוטה ונוחה.

## Usage
הסינטקס הבסיסי של הפקודה הוא:
```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-init FILE`: טוען פקודות מתוך הקובץ המצויין.
- `-batch`: מפעיל את המצב האוטומטי, מונע קלט מהמשתמש.
- `-header`: מציג את כותרות העמודות בתוצאות השאילתות.
- `-csv`: מפיק את התוצאות בפורמט CSV.
- `-version`: מציג את גרסת SQLite המותקנת.

## Common Examples
1. **יצירת מסד נתונים חדש:**
   ```bash
   sqlite3 mydatabase.db
   ```

2. **יצירת טבלה חדשה:**
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

3. **הוספת נתונים לטבלה:**
   ```bash
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
   ```

4. **שאילתת נתונים:**
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

5. **ייצוא נתונים לפורמט CSV:**
   ```bash
   sqlite3 -header -csv mydatabase.db "SELECT * FROM users;" > users.csv
   ```

## Tips
- השתמש באופציה `-init` כדי לטעון פקודות מראש מתוך קובץ, זה יכול לחסוך זמן.
- תמיד גבה את מסדי הנתונים שלך לפני ביצוע שינויים משמעותיים.
- נצל את האפשרות `-batch` כאשר אתה רוצה להריץ פקודות אוטומטיות מבלי להמתין לקלט מהמשתמש.