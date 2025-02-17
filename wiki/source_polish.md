# [Linux] Bash source użycie: Wykonywanie skryptów w bieżącym powłoce

## Overview
Polecenie `source` w Bashu służy do wykonywania skryptów lub plików konfiguracyjnych w bieżącej powłoce. Dzięki temu zmiany wprowadzone w zmiennych środowiskowych lub funkcjach są dostępne w aktualnej sesji terminala.

## Usage
Podstawowa składnia polecenia `source` jest następująca:

```bash
source [opcje] [argumenty]
```

Można również użyć skrótu `.` (kropka) zamiast `source`:

```bash
. [opcje] [argumenty]
```

## Common Options
- `-h`, `--help`: Wyświetla pomoc dotyczącą użycia polecenia.
- `-V`, `--version`: Wyświetla wersję polecenia.

## Common Examples

### Wykonanie skryptu
Aby wykonać skrypt o nazwie `myscript.sh` w bieżącej powłoce, użyj polecenia:

```bash
source myscript.sh
```

### Użycie kropki jako skrótu
Możesz również użyć kropki zamiast `source`:

```bash
. myscript.sh
```

### Ładowanie zmiennych środowiskowych
Jeśli masz plik konfiguracyjny, na przykład `.env`, który zawiera zmienne środowiskowe, możesz je załadować w ten sposób:

```bash
source .env
```

### Wykonanie skryptu z argumentami
Możesz przekazać argumenty do skryptu, który jest wykonywany za pomocą `source`:

```bash
source myscript.sh arg1 arg2
```

## Tips
- Upewnij się, że skrypt, który chcesz wykonać, ma odpowiednie uprawnienia do odczytu.
- Używaj `source` do ładowania plików konfiguracyjnych, aby uniknąć konieczności ponownego uruchamiania powłoki.
- Pamiętaj, że zmiany wprowadzone przez `source` są dostępne tylko w bieżącej sesji powłoki.