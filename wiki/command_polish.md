# [Linux] Bash command użycie: [wyświetlanie zawartości plików]

## Overview
Polecenie `cat` (concatenate) w systemie Linux służy do wyświetlania zawartości plików tekstowych w terminalu. Może być również używane do łączenia kilku plików w jeden.

## Usage
Podstawowa składnia polecenia `cat` wygląda następująco:

```bash
cat [opcje] [argumenty]
```

## Common Options
- `-n`: Numeruje linie wyjścia.
- `-b`: Numeruje tylko niepuste linie.
- `-E`: Dodaje znak końca linii `$` na końcu każdej linii.
- `-s`: Usuwa puste linie.

## Common Examples
1. Wyświetlenie zawartości pliku:
   ```bash
   cat plik.txt
   ```

2. Łączenie dwóch plików w jeden:
   ```bash
   cat plik1.txt plik2.txt > polaczony.txt
   ```

3. Wyświetlenie zawartości pliku z numeracją linii:
   ```bash
   cat -n plik.txt
   ```

4. Usunięcie pustych linii z wyjścia:
   ```bash
   cat -s plik.txt
   ```

5. Wyświetlenie zawartości pliku z oznaczeniem końca linii:
   ```bash
   cat -E plik.txt
   ```

## Tips
- Używaj `cat` w połączeniu z innymi poleceniami, takimi jak `grep`, aby filtrować wyniki.
- Zamiast `cat` do wyświetlania dużych plików, rozważ użycie `less` lub `more`, aby lepiej zarządzać przewijaniem.
- Pamiętaj, że `cat` może być używane do tworzenia nowych plików, ale upewnij się, że nie nadpisujesz ważnych danych.