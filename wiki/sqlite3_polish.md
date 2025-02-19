# [Linux] C Shell (csh) sqlite3 Użycie: Interakcja z bazą danych SQLite

## Overview
Polecenie `sqlite3` jest interfejsem wiersza poleceń do systemu zarządzania bazą danych SQLite. Umożliwia użytkownikom wykonywanie zapytań SQL, zarządzanie bazami danych oraz manipulowanie danymi w prosty sposób.

## Usage
Podstawowa składnia polecenia `sqlite3` jest następująca:

```bash
sqlite3 [opcje] [argumenty]
```

## Common Options
- `-init <plik>`: Wykonuje polecenia SQL z podanego pliku po uruchomieniu.
- `-batch`: Uruchamia w trybie wsadowym, co oznacza, że nie wyświetla interaktywnego promptu.
- `-header`: Wyświetla nagłówki kolumn w wynikach zapytań.
- `-version`: Wyświetla wersję SQLite.

## Common Examples
1. **Utworzenie nowej bazy danych:**
   ```bash
   sqlite3 nowa_baza.db
   ```

2. **Wykonanie zapytania SQL z pliku:**
   ```bash
   sqlite3 nowa_baza.db -init skrypt.sql
   ```

3. **Wyświetlenie wersji SQLite:**
   ```bash
   sqlite3 -version
   ```

4. **Wykonanie prostego zapytania:**
   ```bash
   sqlite3 nowa_baza.db "SELECT * FROM tabela;"
   ```

5. **Eksportowanie wyników zapytania do pliku CSV:**
   ```bash
   sqlite3 -header -csv nowa_baza.db "SELECT * FROM tabela;" > wyniki.csv
   ```

## Tips
- Zawsze twórz kopie zapasowe swoich baz danych przed wprowadzeniem dużych zmian.
- Używaj opcji `-header`, aby ułatwić czytanie wyników zapytań.
- W trybie wsadowym (opcja `-batch`) możesz automatyzować procesy i skrypty SQL, co jest przydatne w codziennej pracy.