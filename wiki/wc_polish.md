# [Linux] Bash wc użycie: Zliczanie linii, słów i znaków w plikach

## Overview
Polecenie `wc` (word count) w systemie Linux służy do zliczania linii, słów i znaków w plikach tekstowych. Jest to przydatne narzędzie do analizy zawartości plików oraz do szybkiego uzyskiwania informacji o ich wielkości.

## Usage
Podstawowa składnia polecenia `wc` jest następująca:

```bash
wc [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `wc`:

- `-l`: Zlicza tylko linie.
- `-w`: Zlicza tylko słowa.
- `-c`: Zlicza tylko znaki.
- `-m`: Zlicza znaki (w tym znaki multibyte).
- `-L`: Wyświetla długość najdłuższej linii.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `wc`:

1. Zliczanie linii w pliku:
   ```bash
   wc -l plik.txt
   ```

2. Zliczanie słów w pliku:
   ```bash
   wc -w plik.txt
   ```

3. Zliczanie znaków w pliku:
   ```bash
   wc -c plik.txt
   ```

4. Zliczanie linii, słów i znaków jednocześnie:
   ```bash
   wc plik.txt
   ```

5. Zliczanie najdłuższej linii w pliku:
   ```bash
   wc -L plik.txt
   ```

## Tips
- Możesz używać `wc` w połączeniu z innymi poleceniami, na przykład z `cat`, aby zliczać zawartość wielu plików:
  ```bash
  cat plik1.txt plik2.txt | wc
  ```
- Jeśli chcesz zliczać zawartość wielu plików jednocześnie, wystarczy podać ich nazwy jako argumenty:
  ```bash
  wc plik1.txt plik2.txt
  ```
- Pamiętaj, że `wc` działa również na danych wejściowych z potoku, co czyni go bardzo elastycznym narzędziem w skryptach bashowych.