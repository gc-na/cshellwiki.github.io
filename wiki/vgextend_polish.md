# [Linux] Bash vgextend użycie: Rozszerzanie grup woluminów

## Overview
Polecenie `vgextend` służy do rozszerzania istniejącej grupy woluminów (VG) o dodatkowe fizyczne woluminy (PV). Umożliwia to zwiększenie dostępnej przestrzeni w grupie woluminów, co jest przydatne w zarządzaniu pamięcią masową w systemach Linux.

## Usage
Podstawowa składnia polecenia `vgextend` jest następująca:

```bash
vgextend [opcje] [nazwa_grupy_woluminów] [fizyczne_woluminy]
```

## Common Options
- `-l, --extents`: Określa liczbę rozszerzeń, które mają zostać dodane do grupy woluminów.
- `-n, --noheadings`: Wyłącza nagłówki w wyjściu.
- `--test`: Sprawdza, co by się stało, gdyby polecenie zostało wykonane, bez faktycznego wprowadzania zmian.

## Common Examples

1. **Rozszerzenie grupy woluminów o jeden fizyczny wolumin:**

```bash
vgextend moja_grupa /dev/sdb1
```

2. **Rozszerzenie grupy woluminów o kilka fizycznych woluminów:**

```bash
vgextend moja_grupa /dev/sdb1 /dev/sdc1
```

3. **Sprawdzenie, co by się stało, gdyby polecenie zostało wykonane:**

```bash
vgextend --test moja_grupa /dev/sdb1
```

## Tips
- Zawsze upewnij się, że fizyczne woluminy, które chcesz dodać, są odpowiednio sformatowane i dostępne.
- Przed rozszerzeniem grupy woluminów warto wykonać kopię zapasową ważnych danych.
- Użyj opcji `--test`, aby zweryfikować skutki polecenia przed jego wykonaniem.