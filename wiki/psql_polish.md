# [Linux] Bash psql Użycie: interakcja z bazą danych PostgreSQL

## Overview
Polecenie `psql` jest interaktywnym narzędziem do zarządzania bazą danych PostgreSQL. Umożliwia użytkownikom wykonywanie zapytań SQL, zarządzanie bazami danych oraz administrację serwerem PostgreSQL.

## Usage
Podstawowa składnia polecenia `psql` wygląda następująco:

```bash
psql [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `psql`:

- `-h` – określa adres hosta serwera PostgreSQL.
- `-U` – pozwala na określenie nazwy użytkownika do logowania.
- `-d` – wskazuje nazwę bazy danych, z którą chcesz się połączyć.
- `-p` – ustawia port, na którym nasłuchuje serwer PostgreSQL.
- `-f` – wykonuje polecenia z pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `psql`:

1. Połączenie z lokalną bazą danych:
   ```bash
   psql -U nazwa_użytkownika -d nazwa_bazy
   ```

2. Połączenie z zdalnym serwerem PostgreSQL:
   ```bash
   psql -h adres_serwera -U nazwa_użytkownika -d nazwa_bazy
   ```

3. Wykonanie zapytania SQL z pliku:
   ```bash
   psql -U nazwa_użytkownika -d nazwa_bazy -f zapytanie.sql
   ```

4. Wyświetlenie listy tabel w bieżącej bazie danych:
   ```bash
   psql -U nazwa_użytkownika -d nazwa_bazy -c "\dt"
   ```

## Tips
- Używaj opcji `-W`, aby wymusić podanie hasła przy logowaniu.
- Możesz korzystać z opcji `\?` w interfejsie `psql`, aby uzyskać pomoc dotyczącą dostępnych poleceń.
- Zapisuj często używane zapytania w plikach, aby móc je łatwo ponownie wykonać.
- Regularnie aktualizuj swoją wersję PostgreSQL, aby korzystać z najnowszych funkcji i poprawek bezpieczeństwa.