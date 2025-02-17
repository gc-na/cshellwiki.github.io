# [লিনাক্স] Bash sqlite3 ব্যবহার: SQLite ডেটাবেস পরিচালনা করুন

## Overview
sqlite3 কমান্ডটি SQLite ডেটাবেস ব্যবস্থাপনার জন্য ব্যবহৃত হয়। এটি একটি হালকা ওজনের ডেটাবেস ইঞ্জিন যা SQL ভাষা ব্যবহার করে ডেটাবেস তৈরি, পরিচালনা এবং প্রশ্ন করার সুবিধা প্রদান করে।

## Usage
sqlite3 কমান্ডের মৌলিক সিনট্যাক্স হলো:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help` : সাহায্যের তথ্য দেখায়।
- `-version` : sqlite3 এর সংস্করণ প্রদর্শন করে।
- `-init <file>` : একটি SQL ফাইল চালানোর জন্য ব্যবহার করা হয়।
- `-batch` : ব্যাচ মোডে কাজ করে, যেখানে কমান্ড লাইন থেকে ইনপুট নেওয়া হয়।

## Common Examples
- একটি নতুন ডেটাবেস তৈরি করা:
```bash
sqlite3 mydatabase.db
```

- একটি টেবিল তৈরি করা:
```bash
sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
```

- একটি রেকর্ড যোগ করা:
```bash
sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
```

- সমস্ত রেকর্ড দেখানো:
```bash
sqlite3 mydatabase.db "SELECT * FROM users;"
```

- একটি SQL ফাইল চালানো:
```bash
sqlite3 mydatabase.db < script.sql
```

## Tips
- ডেটাবেসের ব্যাকআপ নেওয়ার জন্য নিয়মিত `sqlite3` ব্যবহার করুন।
- SQL কমান্ডগুলি একটি ফাইলে সংরক্ষণ করুন এবং সেগুলি একসাথে চালানোর জন্য `-init` অপশন ব্যবহার করুন।
- ডেটাবেসে পরিবর্তন করার আগে সবসময় একটি ব্যাকআপ তৈরি করুন।