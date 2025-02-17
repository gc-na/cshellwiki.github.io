# [Linux] Bash mkfifo użycie: Tworzenie nazwanych potoków

## Overview
Polecenie `mkfifo` służy do tworzenia nazwanych potoków (FIFO) w systemie plików. Nazwane potoki umożliwiają komunikację między procesami w systemie operacyjnym, pozwalając na przesyłanie danych w sposób sekwencyjny.

## Usage
Podstawowa składnia polecenia `mkfifo` jest następująca:

```bash
mkfifo [opcje] [argumenty]
```

## Common Options
- `-m, --mode=MODE` - Ustala uprawnienia dla nowo utworzonego potoku. Można podać tryb w formacie oktalnym (np. `0666`).
- `--help` - Wyświetla pomoc dotyczącą użycia polecenia.
- `--version` - Wyświetla wersję polecenia `mkfifo`.

## Common Examples
1. **Tworzenie prostego potoku:**
   ```bash
   mkfifo mypipe
   ```
   To polecenie tworzy nazwany potok o nazwie `mypipe`.

2. **Tworzenie potoku z określonymi uprawnieniami:**
   ```bash
   mkfifo -m 0644 mypipe
   ```
   Tworzy potok `mypipe` z uprawnieniami do odczytu i zapisu dla właściciela oraz odczytu dla grupy i innych użytkowników.

3. **Użycie potoku w komunikacji między procesami:**
   ```bash
   # W jednym terminalu
   cat < mypipe

   # W drugim terminalu
   echo "Hello, World!" > mypipe
   ```
   W tym przykładzie, tekst "Hello, World!" jest przesyłany przez potok `mypipe` i wyświetlany w pierwszym terminalu.

## Tips
- Upewnij się, że potok jest używany w odpowiednich kontekstach, aby uniknąć zablokowania procesów.
- Sprawdzaj uprawnienia potoku, aby zapewnić odpowiedni dostęp dla procesów, które będą go używać.
- Pamiętaj, że potoki są usuwane automatycznie po zamknięciu wszystkich procesów, które z nich korzystają.