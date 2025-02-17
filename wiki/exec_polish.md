# [Linux] Bash exec użycie: Wykonaj polecenie w bieżącym procesie

## Overview
Polecenie `exec` w Bashu służy do uruchamiania poleceń w bieżącym procesie powłoki, co oznacza, że zastępuje aktualny proces powłoki nowym procesem. Dzięki temu można zmieniać zachowanie powłoki bez konieczności uruchamiania nowej instancji.

## Usage
Podstawowa składnia polecenia `exec` jest następująca:

```bash
exec [opcje] [argumenty]
```

## Common Options
- `-a` : Umożliwia określenie innej nazwy dla uruchamianego polecenia.
- `-l` : Sprawia, że nowe polecenie jest uruchamiane jako login shell.
- `--` : Umożliwia przekazanie argumentów do polecenia, które mogą zaczynać się od `-`.

## Common Examples

### Przykład 1: Zastąpienie powłoki nowym poleceniem
Zastąpienie bieżącej powłoki poleceniem `bash`:

```bash
exec bash
```

### Przykład 2: Uruchomienie programu z inną nazwą
Uruchomienie programu `ls` z inną nazwą:

```bash
exec -a mylist ls -l
```

### Przykład 3: Uruchomienie skryptu jako login shell
Uruchomienie skryptu `myscript.sh` jako login shell:

```bash
exec -l ./myscript.sh
```

### Przykład 4: Przekazywanie argumentów
Uruchomienie polecenia `grep` z przekazaniem argumentów:

```bash
exec grep "tekst" plik.txt
```

## Tips
- Używaj `exec` z ostrożnością, ponieważ zastępuje bieżący proces powłoki, co oznacza, że po jego wykonaniu nie wrócisz do poprzedniego stanu.
- Możesz używać `exec` do zwiększenia wydajności skryptów, eliminując potrzebę tworzenia nowych procesów.
- Sprawdzaj, czy polecenie, które chcesz uruchomić, jest dostępne w systemie, aby uniknąć błędów.