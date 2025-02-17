# [Linux] Bash who użycie: wyświetlanie aktywnych użytkowników

## Overview
Polecenie `who` w systemie Linux służy do wyświetlania listy aktualnie zalogowanych użytkowników. Informacje te obejmują nazwę użytkownika, terminal, z którego się zalogowali, datę oraz godzinę logowania.

## Usage
Podstawowa składnia polecenia `who` jest następująca:

```bash
who [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `who`:

- `-a`: Wyświetla wszystkie dostępne informacje o użytkownikach.
- `-b`: Pokazuje czas ostatniego uruchomienia systemu.
- `-q`: Wyświetla tylko listę zalogowanych użytkowników oraz ich liczbę.
- `--help`: Wyświetla pomoc dotyczącą użycia polecenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `who`:

1. Wyświetlenie listy wszystkich zalogowanych użytkowników:
   ```bash
   who
   ```

2. Wyświetlenie szczegółowych informacji o użytkownikach:
   ```bash
   who -a
   ```

3. Sprawdzenie czasu ostatniego uruchomienia systemu:
   ```bash
   who -b
   ```

4. Wyświetlenie tylko liczby zalogowanych użytkowników:
   ```bash
   who -q
   ```

## Tips
- Używaj opcji `-a`, aby uzyskać pełny obraz aktywności użytkowników w systemie.
- Regularnie sprawdzaj, kto jest zalogowany, aby monitorować bezpieczeństwo systemu.
- Możesz połączyć `who` z innymi poleceniami, takimi jak `grep`, aby filtrować wyniki według konkretnego użytkownika. Na przykład:
  ```bash
  who | grep username
  ```