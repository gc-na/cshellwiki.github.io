# [Linux] Bash sqlite3 użycie: Interakcja z bazą danych SQLite

## Overview
Polecenie `sqlite3` jest narzędziem wiersza poleceń do interakcji z bazą danych SQLite. Umożliwia tworzenie, modyfikowanie oraz zapytywanie baz danych w formacie SQLite, co czyni je przydatnym dla programistów i administratorów baz danych.

## Usage
Podstawowa składnia polecenia `sqlite3` jest następująca:

```bash
sqlite3 [opcje] [argumenty]
```

## Common Options
- `-help` - Wyświetla pomoc i dostępne opcje.
- `-version` - Pokazuje wersję SQLite.
- `-init <plik>` - Wykonuje polecenia z zadanego pliku po uruchomieniu.
- `-batch` - Włącza tryb wsadowy, co oznacza, że nie będzie interaktywnego promptu.
- `-cmd <polecenie>` - Wykonuje polecenie SQL przed uruchomieniem interaktywnej sesji.

## Common Examples
1. **Utworzenie nowej bazy danych:**
   ```bash
   sqlite3 nowa_baza.db
   ```

2. **Wykonanie zapytania SQL:**
   ```bash
   sqlite3 nowa_baza.db "SELECT * FROM tabela;"
   ```

3. **Importowanie danych z pliku CSV:**
   ```bash
   sqlite3 nowa_baza.db ".mode csv" ".import dane.csv tabela"
   ```

4. **Eksportowanie danych do pliku CSV:**
   ```bash
   sqlite3 nowa_baza.db "SELECT * FROM tabela;" ".mode csv" ".output dane.csv" ".dump" ".exit"
   ```

5. **Wykonanie skryptu SQL z pliku:**
   ```bash
   sqlite3 nowa_baza.db < skrypt.sql
   ```

## Tips
- Zawsze wykonuj kopię zapasową bazy danych przed wprowadzeniem większych zmian.
- Używaj trybu wsadowego dla automatyzacji zadań, aby uniknąć interaktywnego promptu.
- Regularnie sprawdzaj wersję SQLite, aby korzystać z najnowszych funkcji i poprawek.