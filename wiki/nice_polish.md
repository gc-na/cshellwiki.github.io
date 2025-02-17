# [Linux] Bash nice użycie: Ustawianie priorytetu procesów

## Overview
Polecenie `nice` w systemach Unix/Linux służy do uruchamiania procesów z określonym priorytetem. Umożliwia to kontrolowanie, jak dużo zasobów systemowych dany proces może wykorzystać w porównaniu do innych procesów. Domyślnie procesy są uruchamiane z neutralnym priorytetem, ale `nice` pozwala na zwiększenie lub zmniejszenie tego priorytetu.

## Usage
Podstawowa składnia polecenia `nice` jest następująca:

```bash
nice [opcje] [argumenty]
```

## Common Options
- `-n, --adjustment=N`: Ustawia wartość priorytetu. Może być liczbą całkowitą od -20 (najwyższy priorytet) do 19 (najniższy priorytet).
- `-h, --help`: Wyświetla pomoc dotyczącą polecenia.
- `--version`: Wyświetla wersję programu.

## Common Examples
1. Uruchomienie programu `my_script.sh` z domyślnym priorytetem:
   ```bash
   nice ./my_script.sh
   ```

2. Uruchomienie programu `my_script.sh` z priorytetem -10:
   ```bash
   nice -n -10 ./my_script.sh
   ```

3. Uruchomienie programu `my_script.sh` z priorytetem 15:
   ```bash
   nice -n 15 ./my_script.sh
   ```

4. Sprawdzenie aktualnego priorytetu procesów:
   ```bash
   ps -o pid,ni,comm
   ```

## Tips
- Używaj `nice` do uruchamiania procesów, które mogą być zasobożerne, aby nie zakłócały pracy innych ważnych procesów w systemie.
- Pamiętaj, że tylko użytkownik root może ustawić priorytet poniżej 0.
- Możesz używać `renice` do zmiany priorytetu już działających procesów.