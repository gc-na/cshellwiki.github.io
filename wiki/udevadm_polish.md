# [Linux] Bash udevadm użycie: zarządzanie urządzeniami w systemie

## Overview
Polecenie `udevadm` jest narzędziem używanym do zarządzania i monitorowania urządzeń w systemie Linux. Umożliwia interakcję z systemem udev, który jest odpowiedzialny za dynamiczne zarządzanie urządzeniami w systemie operacyjnym.

## Usage
Podstawowa składnia polecenia `udevadm` jest następująca:

```bash
udevadm [opcje] [argumenty]
```

## Common Options
- `info`: Wyświetla informacje o urządzeniu.
- `trigger`: Wywołuje zdarzenia udev dla urządzeń.
- `settle`: Czeka na zakończenie wszystkich zdarzeń udev.
- `control`: Kontroluje działanie demona udev.

## Common Examples
1. **Wyświetlanie informacji o urządzeniu:**
   Aby uzyskać szczegółowe informacje o urządzeniu, użyj polecenia:
   ```bash
   udevadm info --query=all --name=/dev/sda
   ```

2. **Wywoływanie zdarzeń udev:**
   Aby wymusić przetworzenie zdarzeń dla wszystkich urządzeń, użyj:
   ```bash
   udevadm trigger
   ```

3. **Czekanie na zakończenie zdarzeń:**
   Aby poczekać na zakończenie przetwarzania zdarzeń, użyj:
   ```bash
   udevadm settle
   ```

4. **Kontrolowanie demona udev:**
   Aby zatrzymać lub uruchomić demona udev, użyj:
   ```bash
   udevadm control --stop
   ```

## Tips
- Używaj opcji `--verbose`, aby uzyskać więcej informacji podczas wykonywania poleceń.
- Sprawdzaj dokumentację za pomocą `man udevadm`, aby poznać więcej opcji i szczegółów.
- Regularnie monitoruj urządzenia po zmianach w systemie, aby upewnić się, że są one poprawnie rozpoznawane.