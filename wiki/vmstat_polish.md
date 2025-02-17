# [Linux] Bash vmstat użycie: Monitorowanie wydajności systemu

## Overview
Polecenie `vmstat` (Virtual Memory Statistics) służy do monitorowania wydajności systemu operacyjnego, dostarczając informacji o pamięci wirtualnej, procesach, systemie wejścia/wyjścia oraz obciążeniu CPU. Umożliwia to administratorom systemów analizowanie stanu systemu w czasie rzeczywistym.

## Usage
Podstawowa składnia polecenia `vmstat` wygląda następująco:

```bash
vmstat [opcje] [argumenty]
```

## Common Options
- `-a` – Wyświetla informacje o pamięci, w tym pamięć aktywną i nieaktywną.
- `-m` – Pokazuje statystyki pamięci podręcznej.
- `-s` – Wyświetla podsumowanie statystyk pamięci.
- `-t` – Dodaje znacznik czasu do wyjścia.
- `interval` – Określa czas w sekundach między kolejnymi pomiarami.
- `count` – Liczba pomiarów do wykonania.

## Common Examples
Przykłady użycia polecenia `vmstat`:

1. Aby wyświetlić statystyki systemu co 2 sekundy przez 5 razy:
   ```bash
   vmstat 2 5
   ```

2. Aby uzyskać szczegółowe informacje o pamięci, w tym pamięć aktywną i nieaktywną:
   ```bash
   vmstat -a
   ```

3. Aby zobaczyć podsumowanie statystyk pamięci:
   ```bash
   vmstat -s
   ```

4. Aby monitorować system z czasem:
   ```bash
   vmstat -t 1 10
   ```

## Tips
- Regularnie monitoruj system za pomocą `vmstat`, aby zidentyfikować potencjalne problemy z wydajnością.
- Używaj opcji `-a`, aby uzyskać pełniejszy obraz użycia pamięci.
- Zapisuj wyniki do pliku, używając przekierowania, aby móc analizować dane później:
  ```bash
  vmstat 1 10 > vmstat_output.txt
  ```