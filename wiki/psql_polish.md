# [Linux] C Shell (csh) psql użycie: interfejs do zarządzania bazą danych PostgreSQL

## Przegląd
Polecenie `psql` jest interaktywnym narzędziem linii poleceń do zarządzania bazą danych PostgreSQL. Umożliwia użytkownikom wykonywanie zapytań SQL, zarządzanie bazami danych oraz administrację systemu baz danych.

## Użycie
Podstawowa składnia polecenia `psql` jest następująca:

```
psql [opcje] [argumenty]
```

## Częste opcje
- `-h` – określa adres hosta serwera bazy danych.
- `-U` – pozwala na podanie nazwy użytkownika do logowania.
- `-d` – określa nazwę bazy danych, z którą chcesz się połączyć.
- `-p` – ustawia port, na którym nasłuchuje serwer bazy danych.
- `-W` – wymusza podanie hasła przed połączeniem.

## Częste przykłady
1. Połączenie z lokalną bazą danych:
   ```bash
   psql -d nazwa_bazy
   ```

2. Połączenie z serwerem na innym hoście:
   ```bash
   psql -h adres_hosta -U nazwa_użytkownika -d nazwa_bazy
   ```

3. Wykonanie zapytania SQL z pliku:
   ```bash
   psql -d nazwa_bazy -f ścieżka/do/pliku.sql
   ```

4. Wyświetlenie listy tabel w bieżącej bazie danych:
   ```bash
   \dt
   ```

## Wskazówki
- Zawsze używaj opcji `-W`, aby zapewnić bezpieczeństwo hasła.
- Możesz używać polecenia `\?` w `psql`, aby uzyskać pomoc dotyczącą dostępnych poleceń.
- Regularnie wykonuj kopie zapasowe swoich baz danych, aby uniknąć utraty danych.