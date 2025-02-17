# [Linux] Bash stty użycie: Konfiguracja terminala

## Overview
Polecenie `stty` służy do zmiany ustawień terminala w systemach Unix i Linux. Umożliwia użytkownikom dostosowanie sposobu, w jaki terminal interpretuje dane wejściowe i wyjściowe, co może być przydatne w różnych scenariuszach, takich jak zmiana klawiszy funkcyjnych czy ustawienie opóźnień.

## Usage
Podstawowa składnia polecenia `stty` jest następująca:

```bash
stty [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `stty`:

- `-a` - Wyświetla wszystkie aktualne ustawienia terminala.
- `-g` - Zwraca aktualne ustawienia w formacie, który można później użyć do przywrócenia tych ustawień.
- `erase` - Ustala znak, który będzie używany do usuwania ostatniego znaku (domyślnie to Backspace).
- `kill` - Ustala znak, który będzie używany do usuwania całej linii (domyślnie to Ctrl+U).
- `intr` - Ustala znak używany do przerywania procesu (domyślnie to Ctrl+C).

## Common Examples

1. **Wyświetlenie wszystkich ustawień terminala:**

```bash
stty -a
```

2. **Ustawienie klawisza Backspace jako znaku usuwania:**

```bash
stty erase ^H
```

3. **Ustawienie znaku przerywania na Ctrl+C:**

```bash
stty intr ^C
```

4. **Zapisanie aktualnych ustawień do zmiennej:**

```bash
current_settings=$(stty -g)
```

5. **Przywrócenie ustawień z zapisanej zmiennej:**

```bash
stty $current_settings
```

## Tips
- Zawsze sprawdzaj aktualne ustawienia terminala przed wprowadzeniem zmian, aby uniknąć niezamierzonych efektów.
- Używaj opcji `-g`, aby zapisać ustawienia przed ich modyfikacją, co pozwoli na łatwe przywrócenie ich później.
- Eksperymentuj z różnymi ustawieniami w bezpiecznym środowisku, aby zrozumieć, jak wpływają na działanie terminala.