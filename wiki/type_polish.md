# [Linux] Bash typ użycia: [sprawdza typ komendy]

## Overview
Polecenie `type` w Bashu służy do określenia typu podanej komendy. Dzięki temu użytkownik może dowiedzieć się, czy dany element jest wbudowaną komendą, aliasem, funkcją czy zewnętrznym plikiem wykonywalnym.

## Usage
Podstawowa składnia polecenia `type` jest następująca:

```bash
type [opcje] [argumenty]
```

## Common Options
- `-t`: Zwraca tylko typ komendy (np. alias, funkcja, plik).
- `-a`: Wyświetla wszystkie lokalizacje dla danej komendy, jeśli istnieje więcej niż jedna.
- `-p`: Zwraca pełną ścieżkę do pliku wykonywalnego, jeśli komenda jest zewnętrzna.

## Common Examples
1. Sprawdzenie typu komendy:
   ```bash
   type ls
   ```
   Wynik: `ls is aliased to 'ls --color=auto'` (jeśli `ls` jest aliasem).

2. Uzyskanie tylko typu komendy:
   ```bash
   type -t echo
   ```
   Wynik: `builtin`

3. Sprawdzenie wszystkich lokalizacji dla komendy:
   ```bash
   type -a python
   ```
   Wynik: `python is /usr/bin/python` (jeśli istnieje więcej niż jedna lokalizacja).

4. Uzyskanie pełnej ścieżki do pliku wykonywalnego:
   ```bash
   type -p gcc
   ```
   Wynik: `/usr/bin/gcc`

## Tips
- Używaj opcji `-t`, aby szybko sprawdzić typ komendy bez dodatkowych informacji.
- Opcja `-a` jest przydatna, gdy masz zainstalowane różne wersje tej samej komendy i chcesz zobaczyć, gdzie są zlokalizowane.
- Pamiętaj, że `type` działa tylko w kontekście powłoki Bash i nie jest dostępne w innych powłokach, takich jak zsh czy fish.