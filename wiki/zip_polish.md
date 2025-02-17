# [Linux] Bash zip użycie: Kompresja plików

## Overview
Polecenie `zip` służy do kompresji plików i folderów w celu zmniejszenia ich rozmiaru. Tworzy plik archiwum w formacie ZIP, który jest powszechnie używany do przechowywania i przesyłania danych.

## Usage
Podstawowa składnia polecenia `zip` wygląda następująco:

```
zip [opcje] [argumenty]
```

## Common Options
- `-r`: Rekursywnie kompresuje foldery.
- `-e`: Szyfruje archiwum hasłem.
- `-u`: Aktualizuje istniejące pliki w archiwum.
- `-d`: Usuwa pliki z archiwum.
- `-v`: Wyświetla szczegółowe informacje o procesie kompresji.

## Common Examples
1. Kompresja pojedynczego pliku:
   ```bash
   zip archiwum.zip plik.txt
   ```

2. Kompresja wielu plików:
   ```bash
   zip archiwum.zip plik1.txt plik2.txt plik3.txt
   ```

3. Rekursywna kompresja folderu:
   ```bash
   zip -r archiwum.zip folder/
   ```

4. Szyfrowanie archiwum hasłem:
   ```bash
   zip -e archiwum.zip plik.txt
   ```

5. Aktualizacja pliku w istniejącym archiwum:
   ```bash
   zip -u archiwum.zip plik.txt
   ```

## Tips
- Używaj opcji `-r`, gdy chcesz skompresować cały folder, aby nie pomijać żadnych plików.
- Pamiętaj o używaniu silnych haseł, gdy szyfrujesz archiwa, aby zapewnić bezpieczeństwo danych.
- Regularnie aktualizuj archiwa, aby mieć pewność, że zawierają najnowsze wersje plików.