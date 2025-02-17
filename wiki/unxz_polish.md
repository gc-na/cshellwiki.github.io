# [Linux] Bash unxz użycie: Rozpakowywanie plików .xz

## Overview
Polecenie `unxz` służy do dekompresji plików skompresowanych za pomocą algorytmu XZ. Jest to narzędzie, które pozwala na przywrócenie oryginalnych danych z plików o rozszerzeniu .xz.

## Usage
Podstawowa składnia polecenia `unxz` jest następująca:

```bash
unxz [opcje] [argumenty]
```

## Common Options
- `-k`, `--keep`: Zachowuje oryginalny plik .xz po dekompresji.
- `-f`, `--force`: Wymusza dekompresję, nawet jeśli plik docelowy już istnieje.
- `-v`, `--verbose`: Wyświetla szczegółowe informacje o postępie dekompresji.

## Common Examples
1. **Dekomprensja pojedynczego pliku:**
   ```bash
   unxz plik.xz
   ```

2. **Zachowanie oryginalnego pliku:**
   ```bash
   unxz -k plik.xz
   ```

3. **Wymuszenie dekompresji:**
   ```bash
   unxz -f plik.xz
   ```

4. **Dekomprensja z wyświetlaniem szczegółów:**
   ```bash
   unxz -v plik.xz
   ```

## Tips
- Zawsze sprawdzaj, czy masz wystarczająco dużo miejsca na dysku przed dekompresją, aby uniknąć problemów z brakiem miejsca.
- Używaj opcji `-k`, jeśli chcesz zachować oryginalny plik, co może być przydatne w przypadku błędów podczas dekompresji.
- Regularnie aktualizuj swoje narzędzia do dekompresji, aby korzystać z najnowszych funkcji i poprawek bezpieczeństwa.