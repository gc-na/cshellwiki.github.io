# [Linux] C Shell (csh) htop użycie: Monitorowanie procesów systemowych

## Overview
Polecenie `htop` jest interaktywnym narzędziem do monitorowania procesów w systemie Linux. Umożliwia użytkownikom przeglądanie aktywnych procesów w czasie rzeczywistym oraz zarządzanie nimi w bardziej przyjazny sposób niż tradycyjne narzędzie `top`.

## Usage
Podstawowa składnia polecenia `htop` jest następująca:

```csh
htop [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `htop`:

- `-h`, `--help`: Wyświetla pomoc i dostępne opcje.
- `-s`, `--sort`: Umożliwia sortowanie procesów według określonego kryterium, np. CPU lub pamięci.
- `-p`, `--pid`: Monitoruje tylko procesy o podanym identyfikatorze PID.
- `-u`, `--user`: Wyświetla procesy tylko dla określonego użytkownika.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `htop`:

1. Uruchomienie `htop` bez żadnych opcji:
   ```csh
   htop
   ```

2. Uruchomienie `htop` z sortowaniem według użycia CPU:
   ```csh
   htop -s PERCENT_CPU
   ```

3. Monitorowanie procesów dla konkretnego użytkownika:
   ```csh
   htop -u username
   ```

4. Monitorowanie konkretnego procesu za pomocą PID:
   ```csh
   htop -p 1234
   ```

## Tips
- Aby zakończyć działanie `htop`, naciśnij klawisz `q`.
- Możesz używać klawiszy strzałek do nawigacji po procesach oraz klawisza `F9`, aby zakończyć wybrany proces.
- Regularnie aktualizuj widok, naciskając klawisz `F5`, aby uzyskać najnowsze informacje o procesach.