# [Linux] Bash sleep użycie: Wstrzymaj wykonywanie skryptu na określony czas

## Overview
Polecenie `sleep` w Bash służy do wstrzymywania wykonywania skryptu na określony czas. Jest to przydatne, gdy chcemy wprowadzić opóźnienia pomiędzy różnymi poleceniami lub operacjami w skryptach.

## Usage
Podstawowa składnia polecenia `sleep` jest następująca:

```bash
sleep [opcje] [czas]
```

## Common Options
- `-h`, `--help`: Wyświetla pomoc dotyczącą polecenia.
- `-V`, `--version`: Wyświetla wersję polecenia.

## Common Examples

1. **Wstrzymaj na 5 sekund:**
   ```bash
   sleep 5
   ```
   To polecenie wstrzyma wykonywanie skryptu na 5 sekund.

2. **Wstrzymaj na 2 minuty:**
   ```bash
   sleep 2m
   ```
   Użycie `m` oznacza minuty, więc to polecenie wstrzyma skrypt na 2 minuty.

3. **Wstrzymaj na 30 sekund:**
   ```bash
   sleep 30
   ```
   Wstrzymuje wykonywanie na 30 sekund.

4. **Wstrzymaj na 1 godzinę:**
   ```bash
   sleep 1h
   ```
   Użycie `h` oznacza godziny, co wstrzyma skrypt na 1 godzinę.

5. **Wstrzymaj w pętli:**
   ```bash
   for i in {1..5}; do
       echo "Wstrzymanie na 1 sekundę..."
       sleep 1
   done
   ```
   Ten skrypt wstrzyma wykonywanie na 1 sekundę pięć razy, wyświetlając komunikat za każdym razem.

## Tips
- Używaj `sleep` w skryptach, aby uniknąć przeciążenia zasobów, zwłaszcza w pętlach.
- Możesz łączyć różne jednostki czasu, np. `sleep 1m30s`, aby wstrzymać na 1 minutę i 30 sekund.
- W przypadku długich operacji, rozważ dodanie komunikatów informacyjnych przed i po `sleep`, aby użytkownicy wiedzieli, co się dzieje.