# [Linux] Bash sqlite3 Χρήση: Διαχείριση βάσεων δεδομένων SQLite

## Overview
Η εντολή `sqlite3` χρησιμοποιείται για την αλληλεπίδραση με βάσεις δεδομένων SQLite. Επιτρέπει στους χρήστες να δημιουργούν, να τροποποιούν και να διαχειρίζονται βάσεις δεδομένων μέσω της γραμμής εντολών.

## Usage
Η βασική σύνταξη της εντολής είναι η εξής:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Εμφανίζει τη βοήθεια για την εντολή.
- `-version`: Εμφανίζει την έκδοση του SQLite.
- `-init <file>`: Εκτελεί εντολές από το καθορισμένο αρχείο κατά την εκκίνηση.
- `-batch`: Εκτελεί τις εντολές χωρίς να περιμένει για είσοδο από τον χρήστη.

## Common Examples
### Δημιουργία νέας βάσης δεδομένων
```bash
sqlite3 mydatabase.db
```

### Εκτέλεση SQL εντολών από αρχείο
```bash
sqlite3 mydatabase.db < script.sql
```

### Δημιουργία πίνακα
```bash
sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
```

### Εισαγωγή δεδομένων
```bash
sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Γιάννης');"
```

### Επιλογή δεδομένων
```bash
sqlite3 mydatabase.db "SELECT * FROM users;"
```

## Tips
- Χρησιμοποιήστε το `-init` για να εκτελέσετε ένα σύνολο εντολών κατά την εκκίνηση της βάσης δεδομένων.
- Αποθηκεύστε τα SQL scripts σας σε αρχεία για εύκολη επαναχρησιμοποίηση.
- Χρησιμοποιήστε το `-batch` για αυτοματοποιημένες διαδικασίες χωρίς αλληλεπίδραση.