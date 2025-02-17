# [Linux] Bash write użycie: Wysyłanie wiadomości do innych użytkowników

## Overview
Polecenie `write` w systemie Linux umożliwia wysyłanie wiadomości tekstowych do innych użytkowników zalogowanych na tym samym systemie. Jest to przydatne narzędzie do komunikacji w czasie rzeczywistym, szczególnie w środowiskach wieloużytkownikowych.

## Usage
Podstawowa składnia polecenia `write` jest następująca:

```bash
write [opcje] [użytkownik] [terminal]
```

## Common Options
- `-n`: Nie wyświetla komunikatu o rozpoczęciu pisania.
- `-h`: Wyświetla pomoc dotycząca użycia polecenia.

## Common Examples
1. Wysyłanie wiadomości do użytkownika `janek`:
   ```bash
   write janek
   Cześć Janek, jak się masz?
   ```

2. Wysyłanie wiadomości do użytkownika `ania` na terminalu `pts/1`:
   ```bash
   write ania pts/1
   Spotkajmy się o 15:00!
   ```

3. Wysyłanie wiadomości bez komunikatu o rozpoczęciu pisania:
   ```bash
   write -n janek
   Pracuję nad projektem, zadzwoń później.
   ```

## Tips
- Upewnij się, że użytkownik, do którego chcesz wysłać wiadomość, jest zalogowany i ma otwarty terminal.
- Aby zakończyć pisanie wiadomości, naciśnij `Ctrl+D`, co sygnalizuje koniec wiadomości.
- Możesz używać `write` w połączeniu z innymi poleceniami, aby automatyzować wysyłanie wiadomości w skryptach.