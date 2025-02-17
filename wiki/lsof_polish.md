# [Linux] Bash lsof Użycie: Wyświetlanie otwartych plików i procesów

## Overview
Polecenie `lsof` (list open files) służy do wyświetlania informacji o otwartych plikach i procesach, które je wykorzystują. Dzięki temu można zidentyfikować, które procesy mają dostęp do określonych plików, co jest przydatne w diagnostyce systemu i zarządzaniu zasobami.

## Usage
Podstawowa składnia polecenia `lsof` jest następująca:

```bash
lsof [opcje] [argumenty]
```

## Common Options
- `-i`: Wyświetla otwarte pliki związane z siecią.
- `-u [użytkownik]`: Pokazuje pliki otwarte przez określonego użytkownika.
- `-p [PID]`: Wyświetla pliki otwarte przez proces o podanym identyfikatorze PID.
- `+D [katalog]`: Rekurencyjnie pokazuje pliki otwarte w danym katalogu.
- `-t`: Zwraca tylko identyfikatory procesów (PID) bez dodatkowych informacji.

## Common Examples
1. Wyświetlenie wszystkich otwartych plików:
   ```bash
   lsof
   ```

2. Wyświetlenie otwartych plików przez określonego użytkownika:
   ```bash
   lsof -u janek
   ```

3. Sprawdzenie, które procesy korzystają z portu 80:
   ```bash
   lsof -i :80
   ```

4. Wyświetlenie plików otwartych przez proces o PID 1234:
   ```bash
   lsof -p 1234
   ```

5. Rekurencyjne wyświetlenie plików otwartych w katalogu `/var/log`:
   ```bash
   lsof +D /var/log
   ```

## Tips
- Używaj opcji `-n` i `-P`, aby przyspieszyć działanie `lsof`, unikając rozwiązywania nazw hostów i portów.
- Regularnie monitoruj otwarte pliki, aby zidentyfikować potencjalne problemy z zasobami.
- Pamiętaj, że do uruchomienia `lsof` mogą być wymagane uprawnienia administratora, aby uzyskać pełne informacje o wszystkich procesach.