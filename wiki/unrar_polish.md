# [Linux] Bash unrar użycie: Rozpakowywanie archiwów RAR

## Overview
Polecenie `unrar` służy do rozpakowywania plików archiwum w formacie RAR. Umożliwia użytkownikom wydobywanie zawartości archiwów RAR, co jest przydatne w przypadku pobierania plików z Internetu lub pracy z danymi skompresowanymi.

## Usage
Podstawowa składnia polecenia `unrar` jest następująca:

```bash
unrar [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `unrar`:

- `x` - Wydobywa pliki z archiwum do bieżącego katalogu, zachowując strukturę folderów.
- `e` - Wydobywa pliki z archiwum do bieżącego katalogu, nie zachowując struktury folderów.
- `l` - Wyświetla listę plików w archiwum.
- `t` - Sprawdza integralność archiwum.
- `v` - Wyświetla szczegółowe informacje o plikach w archiwum.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `unrar`:

1. Aby wydobyć wszystkie pliki z archiwum RAR do bieżącego katalogu, użyj:

   ```bash
   unrar x archiwum.rar
   ```

2. Aby wydobyć pliki z archiwum RAR bez zachowywania struktury folderów, użyj:

   ```bash
   unrar e archiwum.rar
   ```

3. Aby wyświetlić listę plików w archiwum RAR, użyj:

   ```bash
   unrar l archiwum.rar
   ```

4. Aby sprawdzić integralność archiwum RAR, użyj:

   ```bash
   unrar t archiwum.rar
   ```

5. Aby uzyskać szczegółowe informacje o plikach w archiwum, użyj:

   ```bash
   unrar v archiwum.rar
   ```

## Tips
- Upewnij się, że masz zainstalowane odpowiednie pakiety, aby korzystać z polecenia `unrar`, ponieważ nie zawsze jest domyślnie dostępne w systemie.
- Zawsze sprawdzaj integralność archiwum przed jego rozpakowaniem, aby uniknąć problemów z uszkodzonymi plikami.
- Możesz używać opcji `-o+` z poleceniem `unrar`, aby automatycznie nadpisywać istniejące pliki bez pytania.