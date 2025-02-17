# [Linux] Bash env użycie: zarządzanie zmiennymi środowiskowymi

## Overview
Polecenie `env` służy do wyświetlania lub modyfikowania zmiennych środowiskowych w systemie operacyjnym. Umożliwia uruchamianie programów w zmodyfikowanym środowisku, co jest przydatne w różnych scenariuszach, takich jak testowanie lub uruchamianie aplikacji z określonymi ustawieniami.

## Usage
Podstawowa składnia polecenia `env` jest następująca:

```bash
env [options] [arguments]
```

## Common Options
- `-i`: Uruchamia polecenie w pustym środowisku, bez żadnych zmiennych środowiskowych.
- `-u VAR`: Usuwa zmienną środowiskową o nazwie VAR przed uruchomieniem polecenia.
- `VAR=value`: Ustawia zmienną środowiskową VAR na wartość value przed uruchomieniem polecenia.

## Common Examples
1. **Wyświetlenie wszystkich zmiennych środowiskowych:**
   ```bash
   env
   ```

2. **Uruchomienie programu z określoną zmienną środowiskową:**
   ```bash
   env MY_VAR=hello ./my_script.sh
   ```

3. **Usunięcie zmiennej środowiskowej przed uruchomieniem polecenia:**
   ```bash
   env -u MY_VAR ./my_script.sh
   ```

4. **Uruchomienie polecenia w pustym środowisku:**
   ```bash
   env -i bash
   ```

## Tips
- Używaj `env` do testowania aplikacji w różnych konfiguracjach środowiskowych bez zmiany globalnych ustawień.
- Przy uruchamianiu skryptów, które wymagają specyficznych zmiennych, zawsze możesz je ustawić za pomocą `env`, co zwiększa przenośność skryptów.
- Pamiętaj, że zmienne ustawione za pomocą `env` są dostępne tylko dla uruchamianego polecenia i nie wpływają na bieżące środowisko użytkownika.