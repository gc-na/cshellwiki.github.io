# [Linux] Bash top użycie: monitorowanie procesów systemowych

## Overview
Polecenie `top` jest narzędziem do monitorowania procesów działających w systemie Linux. Wyświetla dynamiczny widok procesów, umożliwiając użytkownikom obserwację zużycia zasobów systemowych, takich jak CPU i pamięć.

## Usage
Podstawowa składnia polecenia `top` wygląda następująco:

```bash
top [opcje]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `top`:

- `-d <czas>`: Ustawia czas odświeżania w sekundach.
- `-u <użytkownik>`: Filtruje procesy według określonego użytkownika.
- `-p <PID>`: Monitoruje tylko procesy o podanym identyfikatorze procesu (PID).
- `-n <liczba>`: Określa liczbę odświeżeń, po których `top` zakończy działanie.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `top`:

1. Uruchomienie `top` z domyślnymi ustawieniami:
   ```bash
   top
   ```

2. Ustawienie czasu odświeżania na 2 sekundy:
   ```bash
   top -d 2
   ```

3. Monitorowanie procesów tylko dla konkretnego użytkownika:
   ```bash
   top -u username
   ```

4. Monitorowanie konkretnego procesu za pomocą jego PID:
   ```bash
   top -p 1234
   ```

5. Ograniczenie liczby odświeżeń do 5:
   ```bash
   top -n 5
   ```

## Tips
- Aby zakończyć działanie `top`, naciśnij klawisz `q`.
- Możesz sortować procesy według różnych kryteriów, takich jak zużycie CPU lub pamięci, klikając odpowiednie nagłówki w interfejsie `top`.
- Użyj klawiszy `h` w interfejsie `top`, aby uzyskać pomoc dotyczącą dostępnych skrótów klawiszowych i opcji.