# [לינוקס] Bash groupmod שימוש: שינוי קבוצות במערכת

## Overview
הפקודה `groupmod` משמשת לשינוי מאפיינים של קבוצות במערכת לינוקס. באמצעות הפקודה הזו, ניתן לשנות את שם הקבוצה או את מזהה הקבוצה (GID) שלה.

## Usage
התחביר הבסיסי של הפקודה הוא:

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name`: לשנות את שם הקבוצה.
- `-g, --gid`: לשנות את מזהה הקבוצה (GID).
- `-o`: מאפשר שימוש ב-GID שאינו ייחודי (אם יש צורך).

## Common Examples
שינוי שם של קבוצה:

```bash
groupmod -n newgroup oldgroup
```

שינוי GID של קבוצה:

```bash
groupmod -g 1001 mygroup
```

שינוי גם שם וגם GID של קבוצה:

```bash
groupmod -n newgroup -g 1002 oldgroup
```

## Tips
- תמיד כדאי לבדוק את הקבוצות הקיימות במערכת לפני ביצוע שינויים, באמצעות הפקודה `getent group`.
- אם אתה משנה GID של קבוצה, ודא שהמשתמשים בקבוצה מעודכנים עם ה-GID החדש כדי למנוע בעיות גישה.