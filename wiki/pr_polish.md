# [Linux] C Shell (csh) pr: formatowanie plików tekstowych

## Overview
Polecenie `pr` jest używane do formatowania plików tekstowych w celu ich lepszego wyświetlania na ekranie lub podczas drukowania. Umożliwia podział tekstu na strony, dodawanie nagłówków oraz dostosowywanie szerokości kolumn.

## Usage
Podstawowa składnia polecenia `pr` jest następująca:

```
pr [opcje] [argumenty]
```

## Common Options
- `-h` : Umożliwia dodanie nagłówka do każdej strony.
- `-l` : Określa liczbę linii na stronie.
- `-w` : Ustawia szerokość strony.
- `-t` : Wyłącza nagłówki i stopki.

## Common Examples
Przykłady użycia polecenia `pr`:

1. **Formatowanie pliku tekstowego z domyślnymi ustawieniami:**
   ```csh
   pr dokument.txt
   ```

2. **Dodanie nagłówka do strony:**
   ```csh
   pr -h "Mój dokument" dokument.txt
   ```

3. **Ustawienie liczby linii na stronie na 50:**
   ```csh
   pr -l 50 dokument.txt
   ```

4. **Ustawienie szerokości strony na 80 znaków:**
   ```csh
   pr -w 80 dokument.txt
   ```

5. **Wyłączenie nagłówków i stopek:**
   ```csh
   pr -t dokument.txt
   ```

## Tips
- Używaj opcji `-h`, aby dodać kontekst do wydruku, co może być przydatne podczas przeglądania dokumentów.
- Eksperymentuj z różnymi wartościami opcji `-l` i `-w`, aby znaleźć najlepsze ustawienia dla twojego dokumentu.
- Możesz łączyć różne opcje, aby uzyskać bardziej złożone formatowanie, na przykład:
  ```csh
  pr -h "Mój dokument" -l 40 -w 100 dokument.txt
  ```