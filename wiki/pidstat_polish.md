# [Linux] C Shell (csh) pidstat: Monitorowanie statystyk procesów

## Overview
Polecenie `pidstat` jest używane do monitorowania statystyk procesów w systemie operacyjnym. Umożliwia użytkownikom śledzenie zużycia CPU, pamięci i innych zasobów przez poszczególne procesy w czasie rzeczywistym.

## Usage
Podstawowa składnia polecenia `pidstat` wygląda następująco:

```bash
pidstat [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `pidstat`:

- `-h`: Wyświetla nagłówki w formacie bardziej czytelnym.
- `-r`: Pokazuje statystyki pamięci dla procesów.
- `-u`: Wyświetla statystyki użycia CPU.
- `-p <pid>`: Monitoruje tylko procesy o podanym identyfikatorze PID.
- `-t`: Pokazuje statystyki dla wszystkich wątków procesów.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `pidstat`:

1. Aby monitorować użycie CPU przez wszystkie procesy co 1 sekundę:

    ```bash
    pidstat 1
    ```

2. Aby wyświetlić statystyki pamięci dla wszystkich procesów:

    ```bash
    pidstat -r
    ```

3. Aby monitorować tylko konkretny proces o PID 1234:

    ```bash
    pidstat -p 1234
    ```

4. Aby uzyskać szczegółowe informacje o wszystkich wątkach procesów:

    ```bash
    pidstat -t
    ```

## Tips
- Używaj opcji `-h`, aby poprawić czytelność wyników.
- Regularne monitorowanie procesów może pomóc w identyfikacji problemów z wydajnością.
- Połącz `pidstat` z innymi narzędziami, takimi jak `grep`, aby filtrować wyniki według potrzeb.