# [Linux] Bash sort użycie: sortowanie danych

## Overview
Polecenie `sort` w systemie Linux służy do sortowania linii tekstu w plikach lub standardowym wejściu. Umożliwia uporządkowanie danych w porządku rosnącym lub malejącym, co jest przydatne w wielu scenariuszach, takich jak analiza danych czy przygotowywanie raportów.

## Usage
Podstawowa składnia polecenia `sort` wygląda następująco:

```bash
sort [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `sort`:

- `-r`: Sortowanie w porządku malejącym.
- `-n`: Sortowanie numeryczne.
- `-k`: Określenie kolumny do sortowania.
- `-u`: Usunięcie duplikatów z wyników sortowania.
- `-o`: Zapisanie wyników sortowania do pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `sort`:

1. Sortowanie pliku tekstowego w porządku rosnącym:
   ```bash
   sort plik.txt
   ```

2. Sortowanie pliku tekstowego w porządku malejącym:
   ```bash
   sort -r plik.txt
   ```

3. Sortowanie numeryczne:
   ```bash
   sort -n liczby.txt
   ```

4. Sortowanie według określonej kolumny (np. kolumna 2):
   ```bash
   sort -k 2 plik.txt
   ```

5. Usunięcie duplikatów i zapisanie wyników do nowego pliku:
   ```bash
   sort -u plik.txt -o posortowane.txt
   ```

## Tips
- Używaj opcji `-o`, aby bezpośrednio zapisać posortowane dane do pliku, co oszczędza czas i zasoby.
- Zawsze sprawdzaj, czy dane są odpowiednio sformatowane przed sortowaniem, aby uniknąć nieoczekiwanych wyników.
- Możesz łączyć różne opcje, na przykład `sort -n -r`, aby sortować numerycznie w porządku malejącym.