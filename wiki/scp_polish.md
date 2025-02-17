# [Linux] Bash scp użycie: Kopiowanie plików między hostami

## Overview
Polecenie `scp` (Secure Copy Protocol) służy do bezpiecznego kopiowania plików i katalogów między lokalnym a zdalnym systemem lub między dwoma zdalnymi systemami. Używa protokołu SSH do zapewnienia bezpieczeństwa transferu danych.

## Usage
Podstawowa składnia polecenia `scp` jest następująca:

```bash
scp [opcje] [źródło] [cel]
```

## Common Options
- `-r`: Kopiowanie katalogów rekurencyjnie.
- `-P`: Określenie portu SSH (domyślnie 22).
- `-i`: Użycie określonego klucza prywatnego do autoryzacji.
- `-v`: Włączenie trybu szczegółowego, co pozwala na wyświetlenie dodatkowych informacji o transferze.

## Common Examples
1. **Kopiowanie pliku z lokalnego systemu na zdalny:**
   ```bash
   scp lokalny_plik.txt użytkownik@zdalny_host:/ścieżka/do/docelowego/
   ```

2. **Kopiowanie pliku zdalnego do lokalnego systemu:**
   ```bash
   scp użytkownik@zdalny_host:/ścieżka/do/zdalnego_pliku.txt /ścieżka/do/lokalnego/
   ```

3. **Kopiowanie katalogu rekurencyjnie:**
   ```bash
   scp -r lokalny_katalog/ użytkownik@zdalny_host:/ścieżka/do/docelowego/
   ```

4. **Kopiowanie pliku na zdalny host z określonym portem:**
   ```bash
   scp -P 2222 lokalny_plik.txt użytkownik@zdalny_host:/ścieżka/do/docelowego/
   ```

## Tips
- Używaj opcji `-v`, aby uzyskać więcej informacji o transferze, co może pomóc w diagnozowaniu problemów.
- Zawsze upewnij się, że masz odpowiednie uprawnienia do zapisu w docelowej lokalizacji na zdalnym hoście.
- Rozważ użycie kluczy SSH zamiast haseł dla większego bezpieczeństwa i wygody.