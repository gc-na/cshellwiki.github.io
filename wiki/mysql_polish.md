# [Linux] C Shell (csh) mysql użycie: Interakcja z bazą danych MySQL

## Overview
Polecenie `mysql` jest klientem wiersza poleceń dla systemu zarządzania bazą danych MySQL. Umożliwia użytkownikom wykonywanie zapytań SQL, zarządzanie bazami danych oraz interakcję z serwerem MySQL.

## Usage
Podstawowa składnia polecenia `mysql` wygląda następująco:

```bash
mysql [options] [arguments]
```

## Common Options
- `-u [username]`: Określa nazwę użytkownika do logowania się do bazy danych.
- `-p`: Wymusza podanie hasła użytkownika.
- `-h [hostname]`: Określa adres hosta serwera MySQL.
- `-D [database]`: Wskazuje, z jaką bazą danych chcesz pracować.
- `--execute=[query]`: Wykonuje podane zapytanie SQL bez interakcji z użytkownikiem.

## Common Examples
- Aby połączyć się z lokalnym serwerem MySQL jako użytkownik `root`:

```bash
mysql -u root -p
```

- Aby połączyć się z serwerem MySQL na hoście `example.com`:

```bash
mysql -h example.com -u user -p
```

- Aby wykonać zapytanie SQL bezpośrednio z wiersza poleceń:

```bash
mysql -u user -p -e "SHOW DATABASES;"
```

- Aby połączyć się z określoną bazą danych:

```bash
mysql -u user -p -D my_database
```

## Tips
- Zawsze używaj opcji `-p`, aby zabezpieczyć swoje hasło, zamiast podawać je bezpośrednio w wierszu poleceń.
- Możesz używać plików konfiguracyjnych, aby przechowywać dane logowania, co ułatwia dostęp do bazy danych.
- Regularnie twórz kopie zapasowe swoich baz danych, aby uniknąć utraty danych.