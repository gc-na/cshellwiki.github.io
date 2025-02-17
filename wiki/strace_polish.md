# [Linux] Bash strace użycie: Śledzenie wywołań systemowych

## Overview
Polecenie `strace` służy do śledzenia wywołań systemowych oraz sygnałów, które są generowane przez programy w systemie Linux. Umożliwia to analizę interakcji programu z jądrem systemu, co jest szczególnie przydatne w debugowaniu oraz monitorowaniu działania aplikacji.

## Usage
Podstawowa składnia polecenia `strace` jest następująca:

```bash
strace [opcje] [argumenty]
```

## Common Options
- `-c` – podsumowuje statystyki wywołań systemowych.
- `-e` – pozwala na filtrowanie wywołań systemowych według określonego kryterium.
- `-o <plik>` – zapisuje wyjście do wskazanego pliku zamiast na standardowe wyjście.
- `-p <pid>` – śledzi działający proces o podanym identyfikatorze PID.
- `-f` – śledzi również procesy potomne.

## Common Examples
1. **Śledzenie nowego procesu**:
   Aby śledzić wywołania systemowe dla programu `ls`, użyj:
   ```bash
   strace ls
   ```

2. **Zapis wyjścia do pliku**:
   Aby zapisać wyjście do pliku `output.txt`, użyj:
   ```bash
   strace -o output.txt ls
   ```

3. **Podsumowanie wywołań**:
   Aby uzyskać podsumowanie wywołań systemowych, użyj:
   ```bash
   strace -c ls
   ```

4. **Śledzenie działającego procesu**:
   Aby śledzić proces o PID 1234, użyj:
   ```bash
   strace -p 1234
   ```

5. **Filtrowanie wywołań**:
   Aby śledzić tylko wywołania związane z otwieraniem plików, użyj:
   ```bash
   strace -e trace=open ls
   ```

## Tips
- Używaj opcji `-o`, aby uniknąć zagracenia terminala dużą ilością informacji.
- Filtrowanie wywołań za pomocą opcji `-e` może znacznie ułatwić analizę, zwłaszcza w przypadku dużych aplikacji.
- Pamiętaj, że `strace` może wpływać na wydajność śledzonego procesu, dlatego najlepiej używać go w środowisku testowym.