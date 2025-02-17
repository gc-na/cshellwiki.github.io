# [Linux] Bash uname użycie: Wyświetlanie informacji o systemie

## Overview
Polecenie `uname` służy do wyświetlania informacji o systemie operacyjnym, na którym jest uruchomione. Może dostarczyć szczegółowe dane, takie jak nazwa jądra, wersja systemu oraz architektura sprzętowa.

## Usage
Podstawowa składnia polecenia `uname` jest następująca:

```bash
uname [opcje]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `uname`:

- `-a`: Wyświetla wszystkie dostępne informacje o systemie.
- `-s`: Wyświetla nazwę jądra.
- `-n`: Wyświetla nazwę hosta.
- `-r`: Wyświetla wersję jądra.
- `-v`: Wyświetla dodatkowe informacje o wersji jądra.
- `-m`: Wyświetla architekturę sprzętową.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `uname`:

1. Wyświetlenie wszystkich informacji o systemie:

    ```bash
    uname -a
    ```

2. Wyświetlenie tylko nazwy jądra:

    ```bash
    uname -s
    ```

3. Wyświetlenie wersji jądra:

    ```bash
    uname -r
    ```

4. Wyświetlenie architektury sprzętowej:

    ```bash
    uname -m
    ```

## Tips
- Używaj opcji `-a`, aby uzyskać pełny przegląd systemu w jednym poleceniu.
- Możesz łączyć różne opcje, aby uzyskać bardziej szczegółowe informacje.
- Pamiętaj, że `uname` działa w większości systemów Unix i Linux, więc możesz go używać w różnych środowiskach.