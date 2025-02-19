# [Linux] C Shell (csh) lsmod użycie: wyświetlanie załadowanych modułów jądra

## Overview
Polecenie `lsmod` w systemie Linux służy do wyświetlania listy aktualnie załadowanych modułów jądra. Umożliwia użytkownikom monitorowanie i zarządzanie modułami, co jest istotne dla diagnostyki i konfiguracji systemu.

## Usage
Podstawowa składnia polecenia `lsmod` jest następująca:

```csh
lsmod [opcje] [argumenty]
```

## Common Options
- **-h, --help**: Wyświetla pomoc dotycząca użycia polecenia.
- **-n, --no-pager**: Wyświetla wynik bez użycia paginacji, co jest przydatne w skryptach.

## Common Examples
1. Aby wyświetlić wszystkie załadowane moduły jądra:
   ```csh
   lsmod
   ```

2. Aby uzyskać pomoc na temat użycia polecenia:
   ```csh
   lsmod --help
   ```

3. Aby wyświetlić moduły bez paginacji:
   ```csh
   lsmod --no-pager
   ```

## Tips
- Regularnie sprawdzaj listę załadowanych modułów, aby upewnić się, że potrzebne moduły są aktywne.
- Użyj `modprobe` do ładowania lub usuwania modułów, jeśli zauważysz, że brakuje jakiegoś modułu.
- Możesz przekierować wynik `lsmod` do pliku, aby zachować kopię listy modułów:
   ```csh
   lsmod > lista_modulow.txt
   ```