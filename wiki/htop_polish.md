# [Linux] Bash htop użycie: Monitorowanie procesów w czasie rzeczywistym

## Overview
Polecenie `htop` to interaktywne narzędzie do monitorowania procesów w systemie Linux. Umożliwia użytkownikom przeglądanie aktywnych procesów, zużycia pamięci, obciążenia CPU oraz innych istotnych informacji w czasie rzeczywistym. W przeciwieństwie do tradycyjnego polecenia `top`, `htop` oferuje bardziej przyjazny interfejs graficzny oraz możliwość łatwej nawigacji.

## Usage
Podstawowa składnia polecenia `htop` wygląda następująco:

```bash
htop [opcje] [argumenty]
```

## Common Options
- `-h`, `--help`: Wyświetla pomoc i dostępne opcje.
- `-s`, `--sort`: Umożliwia sortowanie procesów według wybranego kryterium (np. CPU, pamięć).
- `-p`, `--pid`: Monitoruje tylko procesy o podanych identyfikatorach PID.
- `-C`, `--no-color`: Uruchamia `htop` w trybie bez kolorów.

## Common Examples
1. **Uruchomienie htop**:
   ```bash
   htop
   ```

2. **Sortowanie procesów według użycia CPU**:
   ```bash
   htop -s PERCENT_CPU
   ```

3. **Monitorowanie konkretnego procesu za pomocą PID**:
   ```bash
   htop -p 1234
   ```

4. **Wyświetlenie pomocy**:
   ```bash
   htop -h
   ```

## Tips
- Użyj klawiszy strzałek do nawigacji po liście procesów i `F9`, aby zakończyć wybrany proces.
- Możesz zmieniać sortowanie procesów w czasie rzeczywistym, klikając na nagłówki kolumn.
- Regularnie monitoruj obciążenie CPU i pamięci, aby zidentyfikować potencjalne problemy z wydajnością systemu.