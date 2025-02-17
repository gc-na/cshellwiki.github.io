# [Linux] Bash mkdir użycie: Tworzenie nowych katalogów

## Overview
Polecenie `mkdir` służy do tworzenia nowych katalogów w systemie plików. Umożliwia użytkownikom organizowanie plików w struktury folderów, co ułatwia zarządzanie danymi.

## Usage
Podstawowa składnia polecenia `mkdir` jest następująca:

```bash
mkdir [opcje] [argumenty]
```

## Common Options
- `-p`: Tworzy katalogi nadrzędne w razie potrzeby. Jeśli katalog nadrzędny nie istnieje, zostanie utworzony.
- `-v`: Wyświetla szczegółowe informacje o tworzonych katalogach.
- `-m`: Ustawia uprawnienia dla nowego katalogu w formacie oktalnym.

## Common Examples
1. Tworzenie pojedynczego katalogu:
   ```bash
   mkdir nowy_katalog
   ```

2. Tworzenie wielu katalogów jednocześnie:
   ```bash
   mkdir katalog1 katalog2 katalog3
   ```

3. Tworzenie katalogu z katalogiem nadrzędnym:
   ```bash
   mkdir -p /ścieżka/do/katalogu/nadrzędnego/nowy_katalog
   ```

4. Tworzenie katalogu i wyświetlenie informacji:
   ```bash
   mkdir -v nowy_katalog
   ```

5. Tworzenie katalogu z określonymi uprawnieniami:
   ```bash
   mkdir -m 755 nowy_katalog
   ```

## Tips
- Używaj opcji `-p`, gdy nie jesteś pewien, czy katalog nadrzędny już istnieje, aby uniknąć błędów.
- Zawsze sprawdzaj uprawnienia katalogu, zwłaszcza gdy tworzysz katalogi w lokalizacjach systemowych.
- Możesz używać `mkdir` w skryptach Bash, aby automatycznie organizować pliki i katalogi.