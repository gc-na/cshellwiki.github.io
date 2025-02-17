# [Linux] Bash tac użycie: Odwraca zawartość pliku

## Overview
Polecenie `tac` w systemie Linux służy do wyświetlania zawartości pliku w odwrotnej kolejności, linia po linii. Nazwa `tac` pochodzi od słowa `cat` odwróconego, co doskonale oddaje jego funkcję.

## Usage
Podstawowa składnia polecenia `tac` jest następująca:

```bash
tac [opcje] [argumenty]
```

## Common Options
- `-b`, `--before`: Wstawia separator przed każdą linią.
- `-r`, `--regex`: Używa wyrażeń regularnych do dopasowania separatorów.
- `-s`, `--separator=SEPARATOR`: Określa separator, który ma być używany zamiast domyślnego znaku nowej linii.

## Common Examples

1. **Odwrócenie zawartości pliku:**
   ```bash
   tac plik.txt
   ```

2. **Odwrócenie zawartości pliku z separatorem:**
   ```bash
   tac -s ";" plik.csv
   ```

3. **Odwrócenie zawartości pliku z użyciem wyrażeń regularnych:**
   ```bash
   tac -r -s "," plik.txt
   ```

4. **Zapisanie odwróconej zawartości do nowego pliku:**
   ```bash
   tac plik.txt > nowy_plik.txt
   ```

## Tips
- Używaj `tac` w połączeniu z innymi poleceniami, takimi jak `grep` czy `sort`, aby uzyskać bardziej zaawansowane wyniki.
- Pamiętaj, że `tac` działa na całych liniach, więc jeśli potrzebujesz odwrócić pojedyncze słowa w liniach, rozważ użycie innych narzędzi, takich jak `awk` lub `sed`.
- Sprawdź, czy plik, który chcesz odwrócić, nie jest zbyt duży, aby uniknąć problemów z pamięcią.