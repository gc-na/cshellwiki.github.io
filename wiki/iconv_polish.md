# [Linux] Bash iconv użycie: Konwersja kodowania znaków

## Overview
Polecenie `iconv` służy do konwersji tekstu między różnymi kodowaniami znaków. Umożliwia użytkownikom przekształcanie plików tekstowych w celu zapewnienia ich zgodności z różnymi systemami i aplikacjami, które mogą wymagać określonego kodowania.

## Usage
Podstawowa składnia polecenia `iconv` jest następująca:

```bash
iconv [opcje] [argumenty]
```

## Common Options
- `-f`, `--from-code=KOD`: Określa kodowanie źródłowe.
- `-t`, `--to-code=KOD`: Określa kodowanie docelowe.
- `-o`, `--output=PLIK`: Zapisuje wynik do określonego pliku.
- `-c`: Pomija niewłaściwe znaki.

## Common Examples
1. Konwersja pliku z kodowania UTF-8 na ISO-8859-1:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. Konwersja pliku z kodowania Windows-1250 na UTF-8:
   ```bash
   iconv -f WINDOWS-1250 -t UTF-8 input.txt -o output.txt
   ```

3. Wyświetlenie przekształconego tekstu w terminalu bez zapisywania do pliku:
   ```bash
   iconv -f UTF-8 -t ASCII//TRANSLIT input.txt
   ```

4. Pomijanie niewłaściwych znaków podczas konwersji:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1//IGNORE input.txt -o output.txt
   ```

## Tips
- Zawsze sprawdzaj, jakie kodowanie jest używane w pliku źródłowym, aby uniknąć błędów konwersji.
- Używaj opcji `-o`, aby zapisać wynik do nowego pliku, co pozwoli na zachowanie oryginału.
- Testuj konwersję na małych plikach, zanim zastosujesz ją na większych zbiorach danych, aby upewnić się, że wszystko działa zgodnie z oczekiwaniami.