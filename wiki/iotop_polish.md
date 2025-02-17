# [Linux] Bash iotop użycie: Monitorowanie użycia dysku przez procesy

## Overview
Polecenie `iotop` jest narzędziem do monitorowania aktywności dyskowej w systemie Linux. Umożliwia użytkownikom śledzenie, które procesy korzystają z dysku oraz ile danych odczytują i zapisują w czasie rzeczywistym.

## Usage
Podstawowa składnia polecenia `iotop` jest następująca:

```bash
iotop [opcje] [argumenty]
```

## Common Options
- `-o`, `--only`: Wyświetla tylko procesy, które aktualnie wykonują operacje I/O.
- `-b`, `--batch`: Uruchamia `iotop` w trybie wsadowym, co jest przydatne do zapisywania wyników do pliku.
- `-n NUM`, `--iterations NUM`: Określa liczbę iteracji, po których `iotop` zakończy działanie.
- `-p PID`, `--pid=PID`: Monitoruje tylko proces o podanym identyfikatorze PID.

## Common Examples
1. **Podstawowe użycie `iotop`:**
   ```bash
   iotop
   ```
   To polecenie uruchomi interfejs użytkownika `iotop`, który wyświetli procesy korzystające z dysku w czasie rzeczywistym.

2. **Wyświetlanie tylko aktywnych procesów I/O:**
   ```bash
   iotop -o
   ```
   Użycie opcji `-o` pozwala na filtrowanie wyników, pokazując tylko te procesy, które w danym momencie wykonują operacje I/O.

3. **Uruchomienie `iotop` w trybie wsadowym:**
   ```bash
   iotop -b -n 5
   ```
   To polecenie uruchomi `iotop` w trybie wsadowym, wykonując 5 iteracji i następnie kończąc działanie.

4. **Monitorowanie konkretnego procesu:**
   ```bash
   iotop -p 1234
   ```
   W tym przykładzie `iotop` będzie monitorować tylko proces o identyfikatorze PID 1234.

## Tips
- Używaj opcji `-o`, aby szybko zidentyfikować procesy, które intensywnie korzystają z dysku.
- W trybie wsadowym (opcja `-b`) możesz przekierować wyjście do pliku, co ułatwia analizę danych później.
- Regularnie monitoruj system, aby zidentyfikować potencjalne problemy z wydajnością związane z operacjami I/O.