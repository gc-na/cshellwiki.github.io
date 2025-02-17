# [Linux] Bash head użycie: wyświetlanie pierwszych linii pliku

## Overview
Polecenie `head` w systemie Linux służy do wyświetlania pierwszych kilku linii pliku tekstowego. Domyślnie pokazuje pierwsze 10 linii, co jest przydatne, gdy chcemy szybko zobaczyć zawartość pliku bez otwierania go w całości.

## Usage
Podstawowa składnia polecenia `head` jest następująca:

```bash
head [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `head`:

- `-n [liczba]`: Określa liczbę linii do wyświetlenia. Na przykład `-n 5` wyświetli pierwsze 5 linii.
- `-c [liczba]`: Wyświetla określoną liczbę bajtów z pliku.
- `-q`: Nie wyświetla nagłówków plików, gdy podano wiele plików.
- `-v`: Zawsze wyświetla nagłówki plików, nawet przy jednym pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `head`:

1. Wyświetlenie pierwszych 10 linii pliku `plik.txt`:
   ```bash
   head plik.txt
   ```

2. Wyświetlenie pierwszych 5 linii pliku `plik.txt`:
   ```bash
   head -n 5 plik.txt
   ```

3. Wyświetlenie pierwszych 20 bajtów z pliku `plik.txt`:
   ```bash
   head -c 20 plik.txt
   ```

4. Wyświetlenie pierwszych 10 linii z dwóch plików `plik1.txt` i `plik2.txt`:
   ```bash
   head plik1.txt plik2.txt
   ```

5. Wyświetlenie pierwszych 10 linii z pliku `plik.txt` z nagłówkiem:
   ```bash
   head -v plik.txt
   ```

## Tips
- Używaj opcji `-n`, aby dostosować liczbę wyświetlanych linii do swoich potrzeb.
- Możesz łączyć `head` z innymi poleceniami, takimi jak `grep`, aby przefiltrować dane przed ich wyświetleniem.
- Jeśli często potrzebujesz wyświetlać różne pliki, rozważ stworzenie aliasu w swoim pliku konfiguracyjnym powłoki, aby uprościć polecenia.