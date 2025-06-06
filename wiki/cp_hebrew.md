# [לינוקס] C Shell (csh) cp שימוש: העתקת קבצים ותיקיות

## Overview
הפקודה `cp` משמשת להעתקת קבצים ותיקיות ממקום אחד לאחר במערכת הקבצים. היא מאפשרת למשתמשים לשכפל קבצים בקלות ובמהירות.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
cp [אפשרויות] [ארגומנטים]
```

## Common Options
- `-i`: שואל אישור לפני החלפת קובץ קיים.
- `-r`: מעתיק תיקיות באופן רקורסיבי.
- `-u`: מעתיק קבצים רק אם הקובץ המקורי חדש יותר או אם הקובץ היעד אינו קיים.
- `-v`: מציג את הקבצים המועתקים במהלך ההעתקה.

## Common Examples
- העתקת קובץ אחד:
  ```csh
  cp file1.txt file2.txt
  ```
- העתקת קובץ לתיקיה:
  ```csh
  cp file1.txt /path/to/directory/
  ```
- העתקת תיקיה באופן רקורסיבי:
  ```csh
  cp -r /path/to/source_directory /path/to/destination_directory
  ```
- העתקת קובץ עם אישור לפני החלפה:
  ```csh
  cp -i file1.txt file2.txt
  ```

## Tips
- תמיד השתמשו באפשרות `-i` כאשר אתם לא בטוחים אם הקובץ היעד קיים, כדי למנוע אובדן נתונים.
- כאשר מעתיקים תיקיות, אל תשכחו להשתמש באפשרות `-r`.
- כדאי לבדוק את הקבצים המועתקים לאחר ההעתקה כדי לוודא שהכל הועתק כראוי.