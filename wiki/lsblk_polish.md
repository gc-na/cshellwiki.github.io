# [Linux] C Shell (csh) lsblk Użycie: Wyświetlanie informacji o blokowych urządzeniach pamięci

## Overview
Polecenie `lsblk` służy do wyświetlania informacji o urządzeniach blokowych w systemie Linux. Umożliwia użytkownikom przeglądanie struktury urządzeń pamięci, takich jak dyski twarde, partycje i inne nośniki danych.

## Usage
Podstawowa składnia polecenia `lsblk` jest następująca:

```bash
lsblk [options] [arguments]
```

## Common Options
- `-a`, `--all`: Wyświetla wszystkie urządzenia, w tym te, które nie są zamontowane.
- `-f`, `--fs`: Pokazuje informacje o systemach plików na urządzeniach.
- `-l`, `--list`: Wyświetla urządzenia w formacie listy, a nie w formie drzewa.
- `-o`, `--output`: Umożliwia wybór, które kolumny mają być wyświetlane.
- `-n`, `--noheadings`: Ukrywa nagłówki kolumn w wynikach.

## Common Examples
- Aby wyświetlić wszystkie urządzenia blokowe w systemie:

```bash
lsblk
```

- Aby wyświetlić szczegółowe informacje o systemach plików:

```bash
lsblk -f
```

- Aby wyświetlić urządzenia w formacie listy:

```bash
lsblk -l
```

- Aby wyświetlić tylko określone kolumny, na przykład nazwę urządzenia i jego rozmiar:

```bash
lsblk -o NAME,SIZE
```

- Aby wyświetlić wszystkie urządzenia, w tym te, które nie są zamontowane:

```bash
lsblk -a
```

## Tips
- Używaj opcji `-f`, aby szybko sprawdzić, jakie systemy plików są zainstalowane na poszczególnych urządzeniach.
- Opcja `-n` jest przydatna, gdy potrzebujesz wyjścia do skryptów, ponieważ eliminuje nagłówki.
- Regularnie sprawdzaj urządzenia blokowe, aby upewnić się, że wszystkie są poprawnie zamontowane i działają.