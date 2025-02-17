# [Linux] Bash sed użycie: Edytowanie tekstu w strumieniu

## Overview
Polecenie `sed` (stream editor) jest potężnym narzędziem do przetwarzania i edytowania tekstu w strumieniu. Umożliwia m.in. modyfikację plików tekstowych, zamianę słów, usuwanie linii oraz wiele innych operacji na danych tekstowych.

## Usage
Podstawowa składnia polecenia `sed` wygląda następująco:

```bash
sed [opcje] [argumenty]
```

## Common Options
- `-e`: Umożliwia dodanie wielu poleceń sed w jednym wywołaniu.
- `-i`: Edytuje plik "w miejscu", co oznacza, że zmiany są zapisywane bezpośrednio w pliku.
- `-n`: Tylko wyświetla linie, które pasują do podanego wzorca, nie wyświetlając wszystkich linii.
- `s/pattern/replacement/`: Podstawowe polecenie do zamiany wzorca na nowy tekst.

## Common Examples
1. **Zamiana słowa w pliku:**
   ```bash
   sed 's/stare/nowe/' plik.txt
   ```
   To polecenie zamienia pierwsze wystąpienie słowa "stare" na "nowe" w każdej linii pliku `plik.txt`.

2. **Zamiana wszystkich wystąpień słowa:**
   ```bash
   sed 's/stare/nowe/g' plik.txt
   ```
   Użycie flagi `g` powoduje, że wszystkie wystąpienia słowa "stare" w każdej linii są zamieniane na "nowe".

3. **Usuwanie linii zawierających wzorzec:**
   ```bash
   sed '/wzorzec/d' plik.txt
   ```
   To polecenie usuwa wszystkie linie, które zawierają "wzorzec" z pliku `plik.txt`.

4. **Edytowanie pliku w miejscu:**
   ```bash
   sed -i 's/stare/nowe/g' plik.txt
   ```
   Dzięki opcji `-i`, zmiany są zapisywane bezpośrednio w pliku `plik.txt`.

5. **Wyświetlanie tylko linii pasujących do wzorca:**
   ```bash
   sed -n '/wzorzec/p' plik.txt
   ```
   To polecenie wyświetla tylko te linie z `plik.txt`, które zawierają "wzorzec".

## Tips
- Zawsze warto zrobić kopię zapasową pliku przed użyciem opcji `-i`, aby uniknąć utraty danych.
- Używaj opcji `-n` w połączeniu z poleceniem `p`, aby kontrolować, które linie są wyświetlane.
- Możesz łączyć wiele poleceń sed, używając opcji `-e`, co pozwala na bardziej złożone operacje w jednym wywołaniu.