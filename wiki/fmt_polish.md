# [Linux] Bash fmt użycie: Formatowanie tekstu

## Overview
Polecenie `fmt` służy do formatowania tekstu, co oznacza, że przekształca tekst w jednolite linie o określonej długości. Jest to przydatne, gdy chcemy poprawić czytelność tekstu lub dostosować go do określonego formatu.

## Usage
Podstawowa składnia polecenia `fmt` wygląda następująco:

```bash
fmt [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `fmt`:

- `-w, --width=NUM` - Ustawia maksymalną długość linii na NUM znaków (domyślnie 75).
- `-s, --split-only` - Dzieli tekst tylko w miejscach, gdzie występują spacje.
- `-u, --uniform` - Używa jednolitego odstępu między wyrazami.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `fmt`:

1. Formatowanie pliku tekstowego do domyślnej długości linii:
   ```bash
   fmt tekst.txt
   ```

2. Ustawienie maksymalnej długości linii na 50 znaków:
   ```bash
   fmt -w 50 tekst.txt
   ```

3. Formatowanie tekstu z zachowaniem tylko miejsc podziału na spacje:
   ```bash
   fmt -s tekst.txt
   ```

4. Użycie opcji `-u` do uzyskania jednolitego odstępu:
   ```bash
   fmt -u tekst.txt
   ```

## Tips
- Używaj opcji `-w`, aby dostosować długość linii do swoich potrzeb, co może być szczególnie przydatne w dokumentach o różnych formatach.
- Jeśli pracujesz z długimi tekstami, warto przetestować różne wartości dla opcji `-w`, aby znaleźć najbardziej czytelny układ.
- Pamiętaj, że `fmt` nie zmienia oryginalnego pliku, chyba że przekierujesz wynik do nowego pliku lub użyjesz opcji `-o`.