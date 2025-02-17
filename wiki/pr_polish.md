# [Linux] Bash pr: Formatowanie plików tekstowych

## Overview
Polecenie `pr` służy do formatowania plików tekstowych w celu ich łatwiejszego przeglądania na ekranie lub drukowania. Umożliwia podział tekstu na kolumny, dodawanie nagłówków oraz numerowanie stron.

## Usage
Podstawowa składnia polecenia `pr` wygląda następująco:

```bash
pr [opcje] [argumenty]
```

## Common Options
- `-h, --header=HEADER` - Ustawia nagłówek dla każdej strony.
- `-n` - Nie numeruje stron.
- `-t` - Nie dodaje pustych linii na początku.
- `-s, --separator=CHAR` - Ustawia znak separatora między kolumnami.
- `-w, --width=N` - Ustawia szerokość strony na N znaków.

## Common Examples
1. **Podstawowe formatowanie pliku**:
   ```bash
   pr plik.txt
   ```

2. **Formatowanie z nagłówkiem**:
   ```bash
   pr -h "Mój nagłówek" plik.txt
   ```

3. **Podział na dwie kolumny**:
   ```bash
   pr -2 plik.txt
   ```

4. **Ustawienie szerokości strony**:
   ```bash
   pr -w 80 plik.txt
   ```

5. **Numerowanie stron**:
   ```bash
   pr -n plik.txt
   ```

## Tips
- Używaj opcji `-t`, aby uzyskać czystszy wydruk bez dodatkowych pustych linii.
- Eksperymentuj z różnymi szerokościami strony, aby dopasować wyjście do swojego ekranu lub formatu drukowania.
- Możesz łączyć różne opcje, aby uzyskać pożądany efekt, na przykład `pr -h "Nagłówek" -2 plik.txt`.