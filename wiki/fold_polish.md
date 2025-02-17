# [Linux] Bash fold użycie: Zawijanie tekstu do określonej szerokości

## Overview
Polecenie `fold` w systemie Linux służy do zawijania tekstu w plikach lub na standardowym wejściu do określonej szerokości. Umożliwia to lepsze formatowanie tekstu, szczególnie w przypadku długich linii, które mogą nie mieścić się w oknie terminala.

## Usage
Podstawowa składnia polecenia `fold` jest następująca:

```bash
fold [opcje] [argumenty]
```

## Common Options
- `-w, --width=WIDTH` - Ustala maksymalną szerokość wiersza (domyślnie 80 znaków).
- `-s, --break=BREAK` - Zawija tekst w najbliższym spacji, aby uniknąć łamania wyrazów.
- `-b, --bytes` - Liczy szerokość wiersza w bajtach zamiast w znakach.
- `-h, --help` - Wyświetla pomoc dotyczącą użycia polecenia.

## Common Examples
Przykłady użycia polecenia `fold`:

1. Zawijanie tekstu w pliku do domyślnej szerokości 80 znaków:
   ```bash
   fold tekst.txt
   ```

2. Zawijanie tekstu w pliku do szerokości 50 znaków:
   ```bash
   fold -w 50 tekst.txt
   ```

3. Zawijanie tekstu z łamaniem w najbliższej spacji:
   ```bash
   fold -s -w 30 tekst.txt
   ```

4. Zawijanie tekstu z użyciem standardowego wejścia:
   ```bash
   echo "To jest bardzo długi tekst, który chcemy zawinąć." | fold -w 20
   ```

## Tips
- Używaj opcji `-s`, aby uniknąć łamania wyrazów, co może poprawić czytelność tekstu.
- Eksperymentuj z różnymi wartościami szerokości, aby znaleźć najlepsze ustawienie dla swojego terminala lub aplikacji.
- Możesz łączyć `fold` z innymi poleceniami, takimi jak `cat` czy `echo`, aby przetwarzać tekst w bardziej złożony sposób.