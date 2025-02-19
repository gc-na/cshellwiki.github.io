# [Linux] C Shell (csh) zip użycie: kompresja plików

## Overview
Polecenie `zip` służy do kompresji plików i tworzenia archiwów w formacie ZIP. Umożliwia zmniejszenie rozmiaru plików, co ułatwia ich przechowywanie i przesyłanie.

## Usage
Podstawowa składnia polecenia `zip` jest następująca:

```csh
zip [opcje] [argumenty]
```

## Common Options
- `-r`: Rekurencyjnie dodaje pliki z podkatalogów.
- `-e`: Szyfruje archiwum hasłem.
- `-u`: Aktualizuje istniejące pliki w archiwum.
- `-d`: Usuwa pliki z archiwum.

## Common Examples
1. Kompresja pojedynczego pliku:
   ```csh
   zip myarchive.zip file.txt
   ```

2. Kompresja wielu plików:
   ```csh
   zip myarchive.zip file1.txt file2.txt file3.txt
   ```

3. Rekurencyjna kompresja katalogu:
   ```csh
   zip -r myarchive.zip myfolder/
   ```

4. Szyfrowanie archiwum:
   ```csh
   zip -e mysecurearchive.zip file.txt
   ```

5. Aktualizacja pliku w archiwum:
   ```csh
   zip -u myarchive.zip file.txt
   ```

## Tips
- Zawsze sprawdzaj rozmiar archiwum po kompresji, aby upewnić się, że pliki zostały prawidłowo skompresowane.
- Używaj opcji `-r`, gdy chcesz skompresować cały katalog, aby nie pominąć żadnych plików.
- Pamiętaj o używaniu silnych haseł, gdy szyfrujesz archiwa, aby zapewnić bezpieczeństwo danych.