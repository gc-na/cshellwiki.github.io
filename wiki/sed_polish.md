# [Linux] C Shell (csh) sed Użycie: Edytowanie tekstu w strumieniu

## Overview
Polecenie `sed` (stream editor) jest narzędziem do przetwarzania tekstu, które umożliwia edytowanie danych w strumieniu. Używa się go do wykonywania różnych operacji na plikach tekstowych, takich jak zamiana, usuwanie lub dodawanie tekstu.

## Usage
Podstawowa składnia polecenia `sed` wygląda następująco:

```bash
sed [opcje] [argumenty]
```

## Common Options
- `-e`: Umożliwia dodanie skryptu sed do przetwarzania.
- `-i`: Edytuje plik w miejscu, bez tworzenia kopii.
- `-n`: Tylko wyświetla linie, które pasują do wzorca.
- `s/pat/replace/`: Zamienia wzorzec `pat` na `replace`.

## Common Examples
1. **Zamiana tekstu w pliku:**
   ```bash
   sed 's/stary/nowy/' plik.txt
   ```
   To polecenie zamienia pierwsze wystąpienie słowa "stary" na "nowy" w każdej linii pliku `plik.txt`.

2. **Zamiana wszystkich wystąpień tekstu:**
   ```bash
   sed 's/stary/nowy/g' plik.txt
   ```
   Użycie flagi `g` powoduje, że wszystkie wystąpienia "stary" w linii zostaną zamienione na "nowy".

3. **Usuwanie linii zawierających wzorzec:**
   ```bash
   sed '/wzorzec/d' plik.txt
   ```
   To polecenie usuwa wszystkie linie, które zawierają "wzorzec" z pliku `plik.txt`.

4. **Edytowanie pliku w miejscu:**
   ```bash
   sed -i 's/stary/nowy/g' plik.txt
   ```
   To polecenie zamienia wszystkie wystąpienia "stary" na "nowy" bezpośrednio w pliku `plik.txt`.

5. **Wyświetlanie tylko linii pasujących do wzorca:**
   ```bash
   sed -n '/wzorzec/p' plik.txt
   ```
   Użycie opcji `-n` sprawia, że `sed` wyświetla tylko te linie, które pasują do podanego wzorca.

## Tips
- Zawsze warto zrobić kopię zapasową pliku przed użyciem opcji `-i`, aby uniknąć nieodwracalnych zmian.
- Możesz łączyć wiele operacji w jednym poleceniu, używając opcji `-e`.
- Używaj wyrażeń regularnych, aby zwiększyć moc i elastyczność polecenia `sed`.