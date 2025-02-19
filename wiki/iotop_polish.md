# [Linux] C Shell (csh) iotop użycie: monitorowanie użycia dysku w czasie rzeczywistym

## Overview
Polecenie `iotop` służy do monitorowania użycia dysku przez procesy w czasie rzeczywistym. Umożliwia użytkownikom śledzenie, które procesy generują największe obciążenie dysku, co może być przydatne w diagnozowaniu problemów z wydajnością systemu.

## Usage
Podstawowa składnia polecenia `iotop` wygląda następująco:

```csh
iotop [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `iotop`:

- `-o` – wyświetla tylko procesy, które aktualnie wykonują operacje I/O.
- `-b` – uruchamia `iotop` w trybie wsadowym, co jest przydatne do zapisywania wyników do pliku.
- `-n NUM` – określa liczbę iteracji, po których `iotop` zakończy działanie.
- `-d SEC` – ustawia czas odświeżania w sekundach.

## Common Examples
Oto kilka praktycznych przykładów użycia `iotop`:

1. Aby uruchomić `iotop` w trybie interaktywnym, wystarczy wpisać:

    ```csh
    iotop
    ```

2. Aby zobaczyć tylko procesy wykonujące operacje I/O:

    ```csh
    iotop -o
    ```

3. Aby uruchomić `iotop` w trybie wsadowym i zapisać wyniki do pliku:

    ```csh
    iotop -b -n 5 > wyniki_iotop.txt
    ```

4. Aby ustawić czas odświeżania na 2 sekundy i wyświetlić tylko procesy I/O:

    ```csh
    iotop -o -d 2
    ```

## Tips
- Używaj opcji `-o`, aby szybko zidentyfikować procesy, które obciążają dysk.
- W trybie wsadowym (`-b`) możesz łatwo zbierać dane do analizy później.
- Pamiętaj, że `iotop` wymaga uprawnień administratora, aby uzyskać pełne informacje o wszystkich procesach. Uruchom go z `sudo`, jeśli to konieczne.