# [Linux] Bash uniq użycie: Usuwa duplikaty z pliku

## Overview
Polecenie `uniq` w systemie Linux służy do usuwania duplikatów z plików tekstowych. Działa na zasadzie porównywania sąsiadujących ze sobą linii i wyświetlania tylko unikalnych wpisów. Aby `uniq` zadziałał poprawnie, dane muszą być posortowane.

## Usage
Podstawowa składnia polecenia `uniq` jest następująca:

```bash
uniq [opcje] [argumenty]
```

## Common Options
- `-c`: Zlicza wystąpienia każdej unikalnej linii i wyświetla je przed linią.
- `-d`: Wyświetla tylko linie, które są duplikatami.
- `-u`: Wyświetla tylko linie, które są unikalne (niepowtarzające się).
- `-i`: Ignoruje wielkość liter podczas porównywania linii.
- `-w N`: Porównuje tylko pierwsze N znaków w każdej linii.

## Common Examples

1. **Usunięcie duplikatów z pliku:**
   ```bash
   uniq plik.txt
   ```

2. **Zliczanie wystąpień unikalnych linii:**
   ```bash
   uniq -c plik.txt
   ```

3. **Wyświetlenie tylko duplikatów:**
   ```bash
   uniq -d plik.txt
   ```

4. **Wyświetlenie tylko unikalnych linii:**
   ```bash
   uniq -u plik.txt
   ```

5. **Ignorowanie wielkości liter:**
   ```bash
   uniq -i plik.txt
   ```

6. **Porównywanie tylko pierwszych N znaków:**
   ```bash
   uniq -w 5 plik.txt
   ```

## Tips
- Upewnij się, że dane w pliku są posortowane przed użyciem `uniq`, aby uzyskać poprawne wyniki.
- Możesz użyć `sort` w połączeniu z `uniq`, aby najpierw posortować dane:
  ```bash
  sort plik.txt | uniq
  ```
- Zawsze sprawdzaj, czy używasz odpowiednich opcji, aby uzyskać pożądany wynik, szczególnie przy dużych zbiorach danych.