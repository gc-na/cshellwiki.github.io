# [Linux] Bash w w: wyświetlanie aktywnych użytkowników i ich aktywności

## Overview
Polecenie `w` w systemie Linux służy do wyświetlania informacji o aktualnie zalogowanych użytkownikach oraz ich aktywności. Umożliwia to administratorom systemu monitorowanie, kto jest zalogowany i co robi w danym momencie.

## Usage
Podstawowa składnia polecenia `w` jest następująca:

```bash
w [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `w`:

- `-h`: Ukrywa nagłówek wyjścia.
- `-s`: Wyświetla skróconą wersję informacji.
- `-f`: Wyświetla pełne informacje o użytkownikach, w tym ich terminale.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `w`:

1. Wyświetlenie podstawowych informacji o zalogowanych użytkownikach:
   ```bash
   w
   ```

2. Wyświetlenie informacji bez nagłówka:
   ```bash
   w -h
   ```

3. Wyświetlenie skróconej wersji informacji:
   ```bash
   w -s
   ```

4. Wyświetlenie pełnych informacji o użytkownikach:
   ```bash
   w -f
   ```

## Tips
- Używaj polecenia `w` regularnie, aby monitorować aktywność użytkowników w systemie.
- Możesz połączyć `w` z innymi poleceniami, takimi jak `grep`, aby filtrować wyniki według konkretnego użytkownika.
- Zwróć uwagę na kolumnę "idle", która pokazuje, jak długo użytkownik był nieaktywny, co może być przydatne w ocenie obciążenia systemu.