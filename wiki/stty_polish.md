# [Linux] C Shell (csh) stty użycie: Ustawianie i wyświetlanie opcji terminala

## Overview
Polecenie `stty` w C Shell (csh) służy do ustawiania i wyświetlania opcji terminala. Umożliwia użytkownikom dostosowanie zachowania terminala, co może być przydatne w różnych scenariuszach, takich jak zmiana ustawień wejścia/wyjścia czy konfiguracja sygnałów.

## Usage
Podstawowa składnia polecenia `stty` jest następująca:

```csh
stty [opcje] [argumenty]
```

## Common Options
Oto niektóre z najczęściej używanych opcji polecenia `stty`:

- `-a`: Wyświetla wszystkie ustawienia terminala.
- `-g`: Zapisuje aktualne ustawienia terminala w formacie, który można później przywrócić.
- `erase`: Ustawia znak do usuwania (domyślnie jest to Backspace).
- `kill`: Ustawia znak do usuwania linii (domyślnie jest to Ctrl+U).
- `intr`: Ustawia znak do przerwania (domyślnie jest to Ctrl+C).

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `stty`:

1. Wyświetlenie wszystkich ustawień terminala:
   ```csh
   stty -a
   ```

2. Ustawienie znaku usuwania na Backspace:
   ```csh
   stty erase ^H
   ```

3. Ustawienie znaku do usuwania linii na Ctrl+X:
   ```csh
   stty kill ^X
   ```

4. Zapisanie aktualnych ustawień terminala do zmiennej:
   ```csh
   stty -g > ustawienia.txt
   ```

5. Przywrócenie ustawień terminala z pliku:
   ```csh
   stty `cat ustawienia.txt`
   ```

## Tips
- Używaj opcji `-a`, aby szybko sprawdzić wszystkie aktualne ustawienia terminala przed wprowadzeniem zmian.
- Zapisuj ustawienia terminala przed ich modyfikacją, aby móc je łatwo przywrócić w razie potrzeby.
- Pamiętaj, że zmiany wprowadzone za pomocą `stty` są tymczasowe i znikną po zamknięciu terminala.