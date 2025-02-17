# [Linux] Bash whoami Użycie: Zwraca nazwę aktualnego użytkownika

## Overview
Polecenie `whoami` w systemie Linux służy do wyświetlania nazwy użytkownika, który aktualnie jest zalogowany w sesji terminala. Jest to przydatne narzędzie do szybkiego sprawdzenia, pod jakim kontem użytkownik pracuje w danym momencie.

## Usage
Podstawowa składnia polecenia `whoami` jest następująca:

```bash
whoami [opcje]
```

## Common Options
Chociaż `whoami` nie ma wielu opcji, oto kilka, które mogą być przydatne:

- `--help`: Wyświetla pomoc dotyczącą polecenia.
- `--version`: Pokazuje wersję programu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `whoami`:

1. **Wyświetlenie nazwy aktualnego użytkownika:**
   ```bash
   whoami
   ```

2. **Wyświetlenie pomocy:**
   ```bash
   whoami --help
   ```

3. **Sprawdzenie wersji polecenia:**
   ```bash
   whoami --version
   ```

## Tips
- Używaj `whoami` w skryptach, aby dynamicznie uzyskiwać informacje o użytkowniku, co może być przydatne w kontekście uprawnień.
- Możesz łączyć `whoami` z innymi poleceniami, aby dostosować skrypty do działania w zależności od zalogowanego użytkownika.
- Pamiętaj, że `whoami` zwraca tylko nazwę użytkownika, a nie inne informacje, takie jak identyfikator użytkownika (UID).