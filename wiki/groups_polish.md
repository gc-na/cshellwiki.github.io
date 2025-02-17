# [Linux] Bash groups użycie: wyświetlanie grup użytkowników

## Overview
Polecenie `groups` w systemie Linux służy do wyświetlania grup, do których należy dany użytkownik. Może być używane do sprawdzenia przynależności do grup oraz do zarządzania uprawnieniami w systemie.

## Usage
Podstawowa składnia polecenia `groups` jest następująca:

```bash
groups [opcje] [argumenty]
```

## Common Options
- `-h`, `--help` - wyświetla pomoc dotyczącą polecenia.
- `-v`, `--version` - wyświetla wersję polecenia.

## Common Examples
1. **Wyświetlenie grup dla bieżącego użytkownika:**

```bash
groups
```

2. **Wyświetlenie grup dla konkretnego użytkownika:**

```bash
groups nazwa_użytkownika
```

3. **Wyświetlenie grup dla wielu użytkowników:**

```bash
groups użytkownik1 użytkownik2
```

## Tips
- Używaj polecenia `groups` bez argumentów, aby szybko sprawdzić, do jakich grup należy aktualnie zalogowany użytkownik.
- Możesz używać `groups` w skryptach, aby dynamicznie sprawdzać uprawnienia użytkowników.
- Pamiętaj, że przynależność do grup wpływa na dostęp do plików i zasobów w systemie, więc warto regularnie monitorować te informacje.