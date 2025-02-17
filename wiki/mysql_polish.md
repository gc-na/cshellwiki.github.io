# [Linux] Bash mysql użycie: Interakcja z bazą danych MySQL

## Overview
Polecenie `mysql` jest klientem wiersza poleceń dla systemu zarządzania bazą danych MySQL. Umożliwia użytkownikom wykonywanie zapytań SQL, zarządzanie bazami danych oraz administrację użytkownikami i uprawnieniami.

## Usage
Podstawowa składnia polecenia `mysql` jest następująca:

```bash
mysql [opcje] [argumenty]
```

## Common Options
- `-u, --user=NAZWA_UŻYTKOWNIKA`: Określa nazwę użytkownika do logowania.
- `-p, --password`: Prosi o hasło użytkownika (można je również podać bezpośrednio po `-p`).
- `-h, --host=HOST`: Określa adres hosta serwera MySQL (domyślnie localhost).
- `-D, --database=NAZWA_BAZY`: Określa bazę danych, z którą chcesz pracować.
- `--execute=ZAPYTANIE`: Wykonuje podane zapytanie SQL bezpośrednio z wiersza poleceń.

## Common Examples

### Połączenie z lokalnym serwerem MySQL
```bash
mysql -u root -p
```
To polecenie łączy się z lokalnym serwerem MySQL jako użytkownik `root` i prosi o hasło.

### Wykonanie zapytania SQL
```bash
mysql -u root -p --execute="SHOW DATABASES;"
```
To polecenie łączy się z serwerem MySQL i wykonuje zapytanie, które wyświetla dostępne bazy danych.

### Połączenie z zdalnym serwerem MySQL
```bash
mysql -h 192.168.1.100 -u user -p
```
To polecenie łączy się z zdalnym serwerem MySQL znajdującym się pod adresem IP `192.168.1.100`.

### Wybór bazy danych
```bash
mysql -u user -p -D my_database
```
To polecenie łączy się z serwerem MySQL i bezpośrednio wybiera bazę danych `my_database`.

## Tips
- Zawsze używaj opcji `-p`, aby zabezpieczyć swoje hasło, zamiast podawać je w linii poleceń.
- Używaj opcji `--execute` do szybkiego wykonywania pojedynczych zapytań bez otwierania interaktywnej sesji.
- Regularnie twórz kopie zapasowe swoich baz danych, aby uniknąć utraty danych.