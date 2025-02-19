# [Linux] C Shell (csh) head użycie: wyświetlanie pierwszych linii pliku

## Overview
Polecenie `head` w C Shell (csh) służy do wyświetlania pierwszych kilku linii pliku tekstowego. Jest to przydatne narzędzie, gdy chcesz szybko zobaczyć zawartość pliku bez otwierania go w pełni.

## Usage
Podstawowa składnia polecenia `head` jest następująca:

```
head [opcje] [argumenty]
```

## Common Options
- `-n [liczba]`: Określa liczbę linii do wyświetlenia. Domyślnie `head` pokazuje 10 linii.
- `-c [liczba]`: Wyświetla określoną liczbę bajtów z początku pliku.
- `-q`: Nie wyświetla nagłówków plików, gdy podano wiele plików.
- `-v`: Zawsze wyświetla nagłówki plików.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `head`:

1. Wyświetlenie pierwszych 10 linii pliku `plik.txt`:
   ```csh
   head plik.txt
   ```

2. Wyświetlenie pierwszych 5 linii pliku `dane.log`:
   ```csh
   head -n 5 dane.log
   ```

3. Wyświetlenie pierwszych 100 bajtów pliku `raport.txt`:
   ```csh
   head -c 100 raport.txt
   ```

4. Wyświetlenie pierwszych 10 linii z dwóch plików `plik1.txt` i `plik2.txt`:
   ```csh
   head plik1.txt plik2.txt
   ```

5. Wyświetlenie pierwszych 10 linii z pliku `plik.txt` z nagłówkiem:
   ```csh
   head -v plik.txt
   ```

## Tips
- Używaj opcji `-n`, aby dostosować liczbę wyświetlanych linii do swoich potrzeb.
- Możesz łączyć `head` z innymi poleceniami, używając potoków, aby analizować dane w czasie rzeczywistym.
- Zawsze sprawdzaj zawartość pliku przed jego edytowaniem, aby uniknąć przypadkowych zmian w ważnych danych.