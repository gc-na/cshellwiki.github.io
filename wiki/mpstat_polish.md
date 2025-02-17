# [Linux] Bash mpstat Użycie: Monitorowanie statystyk CPU

## Overview
Polecenie `mpstat` jest używane do monitorowania wydajności procesora w systemach Linux. Umożliwia użytkownikom zbieranie i wyświetlanie statystyk dotyczących obciążenia CPU, co pozwala na analizę wydajności systemu w czasie rzeczywistym.

## Usage
Podstawowa składnia polecenia `mpstat` jest następująca:

```bash
mpstat [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `mpstat`:

- `-P ALL` - Wyświetla statystyki dla wszystkich rdzeni CPU.
- `-u` - Pokazuje procent czasu, w którym CPU jest w użyciu.
- `-h` - Wyświetla wyniki w formacie bardziej przyjaznym dla użytkownika (np. z jednostkami).
- `-o` - Określa format wyjściowy (np. CSV, JSON).

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `mpstat`:

1. Aby wyświetlić statystyki CPU dla wszystkich rdzeni co 1 sekundę:

   ```bash
   mpstat -P ALL 1
   ```

2. Aby uzyskać tylko procent czasu użycia CPU:

   ```bash
   mpstat -u 1
   ```

3. Aby zapisać statystyki w formacie CSV:

   ```bash
   mpstat -P ALL -o CSV 1 > statystyki.csv
   ```

4. Aby wyświetlić statystyki z użyciem formatu przyjaznego dla użytkownika:

   ```bash
   mpstat -h 1
   ```

## Tips
- Używaj opcji `-P ALL`, aby uzyskać pełny obraz wydajności wszystkich rdzeni CPU, co jest szczególnie przydatne w systemach wielordzeniowych.
- Regularne monitorowanie CPU może pomóc w identyfikacji problemów z wydajnością, dlatego warto ustawić `mpstat` w skrypcie do automatycznego uruchamiania.
- Zapisuj wyniki do pliku, aby móc je analizować później, co ułatwi diagnozowanie problemów z wydajnością.