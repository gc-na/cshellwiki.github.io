# [Linux] Bash getconf użycie: Uzyskiwanie informacji o konfiguracji systemu

## Overview
Polecenie `getconf` służy do uzyskiwania informacji o konfiguracji systemu oraz zmiennych systemowych. Umożliwia dostęp do różnych parametrów systemowych, takich jak maksymalne rozmiary plików, liczba procesów czy inne ustawienia konfiguracyjne.

## Usage
Podstawowa składnia polecenia `getconf` jest następująca:

```bash
getconf [opcje] [argumenty]
```

## Common Options
- `-a`: Wyświetla wszystkie dostępne zmienne konfiguracyjne.
- `-v`: Wyświetla wersję polecenia `getconf`.
- `variable`: Nazwa konkretnej zmiennej, której wartość chcemy uzyskać.

## Common Examples
1. Aby uzyskać wszystkie dostępne zmienne konfiguracyjne, użyj:

    ```bash
    getconf -a
    ```

2. Aby sprawdzić maksymalny rozmiar pliku, użyj:

    ```bash
    getconf _PC_MAX_INPUT
    ```

3. Aby uzyskać wartość konkretnej zmiennej, na przykład liczby procesów, użyj:

    ```bash
    getconf _NPROCESSORS_ONLN
    ```

4. Aby sprawdzić wersję polecenia `getconf`, użyj:

    ```bash
    getconf -v
    ```

## Tips
- Używaj opcji `-a`, aby szybko przeglądać wszystkie dostępne zmienne konfiguracyjne, co może być pomocne w diagnostyce systemu.
- Sprawdzaj konkretne zmienne, aby dostosować skrypty do specyfikacji systemu, co zwiększy ich przenośność.
- Pamiętaj, że niektóre zmienne mogą być różne w zależności od systemu operacyjnego, więc zawsze warto sprawdzić ich dostępność na danym systemie.