# [Linux] C Shell (csh) mv Użycie: Przenoszenie lub zmiana nazw plików

## Overview
Polecenie `mv` w C Shell (csh) służy do przenoszenia plików i katalogów oraz zmiany ich nazw. Jest to podstawowe narzędzie do zarządzania plikami w systemie Unix i Linux.

## Usage
Podstawowa składnia polecenia `mv` jest następująca:

```csh
mv [opcje] [argumenty]
```

## Common Options
- `-i`: Pyta o potwierdzenie przed nadpisaniem istniejącego pliku.
- `-u`: Przenosi plik tylko wtedy, gdy źródło jest nowsze od celu lub gdy cel nie istnieje.
- `-v`: Wyświetla szczegóły operacji przenoszenia.

## Common Examples
1. **Przeniesienie pliku do innego katalogu:**
   ```csh
   mv dokument.txt /home/użytkownik/dokumenty/
   ```

2. **Zmiana nazwy pliku:**
   ```csh
   mv stary_nazwa.txt nowy_nazwa.txt
   ```

3. **Przeniesienie wielu plików do katalogu:**
   ```csh
   mv plik1.txt plik2.txt /home/użytkownik/dokumenty/
   ```

4. **Przeniesienie pliku z potwierdzeniem:**
   ```csh
   mv -i dokument.txt /home/użytkownik/dokumenty/
   ```

5. **Przeniesienie pliku, jeśli jest nowszy:**
   ```csh
   mv -u dokument.txt /home/użytkownik/dokumenty/
   ```

## Tips
- Zawsze używaj opcji `-i`, aby uniknąć przypadkowego nadpisania plików.
- Sprawdzaj, czy plik docelowy już istnieje, aby uniknąć utraty danych.
- Używaj opcji `-v`, aby śledzić, co się dzieje podczas przenoszenia plików.