# [Linux] Bash logrotate użycie: Zarządzanie rotacją plików dziennika

## Overview
Polecenie `logrotate` służy do zarządzania rotacją, kompresją i usuwaniem plików dziennika w systemach Unix i Linux. Umożliwia automatyczne zarządzanie plikami dziennika, co pomaga w oszczędzaniu miejsca na dysku oraz w utrzymaniu porządku w logach.

## Usage
Podstawowa składnia polecenia `logrotate` jest następująca:

```bash
logrotate [opcje] [argumenty]
```

## Common Options
- `-f` : Wymusza rotację plików dziennika, niezależnie od ustawień.
- `-s` : Określa plik stanu, który przechowuje informacje o rotacji.
- `-v` : Włącza tryb szczegółowy, wyświetlając dodatkowe informacje podczas działania.
- `-d` : Uruchamia `logrotate` w trybie testowym, bez wprowadzania zmian.

## Common Examples

### Przykład 1: Podstawowe użycie
Aby wykonać rotację plików dziennika zgodnie z domyślną konfiguracją, użyj:

```bash
logrotate /etc/logrotate.conf
```

### Przykład 2: Wymuszenie rotacji
Aby wymusić rotację plików dziennika, użyj:

```bash
logrotate -f /etc/logrotate.conf
```

### Przykład 3: Uruchomienie w trybie szczegółowym
Aby zobaczyć szczegóły działania `logrotate`, uruchom:

```bash
logrotate -v /etc/logrotate.conf
```

### Przykład 4: Użycie pliku stanu
Aby określić niestandardowy plik stanu, użyj:

```bash
logrotate -s /path/to/custom/state/file /etc/logrotate.conf
```

## Tips
- Regularnie przeglądaj plik konfiguracyjny `/etc/logrotate.conf`, aby dostosować ustawienia do swoich potrzeb.
- Używaj trybu testowego (`-d`), aby upewnić się, że konfiguracja działa poprawnie przed wprowadzeniem zmian.
- Monitoruj pliki dziennika po rotacji, aby upewnić się, że nie występują błędy w procesie rotacji.