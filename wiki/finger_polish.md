# [Linux] C Shell (csh) finger użycie: wyświetlanie informacji o użytkownikach

## Overview
Polecenie `finger` służy do wyświetlania informacji o użytkownikach systemu. Umożliwia uzyskanie szczegółowych danych, takich jak nazwa użytkownika, pełne imię i nazwisko, czas logowania oraz inne informacje związane z kontem użytkownika.

## Usage
Podstawowa składnia polecenia `finger` jest następująca:

```
finger [opcje] [argumenty]
```

## Common Options
- `-l`: Wyświetla szczegółowe informacje o użytkownikach.
- `-m`: Ignoruje wielkość liter w nazwach użytkowników.
- `-s`: Wyświetla skrócone informacje o użytkownikach.

## Common Examples
1. Wyświetlenie informacji o wszystkich użytkownikach:
   ```bash
   finger
   ```

2. Wyświetlenie szczegółowych informacji o konkretnym użytkowniku:
   ```bash
   finger janek
   ```

3. Wyświetlenie skróconych informacji o wszystkich użytkownikach:
   ```bash
   finger -s
   ```

4. Ignorowanie wielkości liter przy wyszukiwaniu użytkownika:
   ```bash
   finger -m Ania
   ```

## Tips
- Używaj opcji `-l`, aby uzyskać pełne informacje o użytkownikach, co może być przydatne w administracji systemu.
- W przypadku dużych systemów, korzystaj z opcji `-s`, aby szybko przeglądać użytkowników bez zbędnych szczegółów.
- Pamiętaj, że dostępność informacji może być ograniczona przez ustawienia prywatności użytkowników.