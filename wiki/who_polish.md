# [Linux] C Shell (csh) who użycie: wyświetla listę zalogowanych użytkowników

## Overview
Polecenie `who` w C Shell (csh) służy do wyświetlania listy użytkowników aktualnie zalogowanych do systemu. Informacje te mogą być przydatne do monitorowania aktywności użytkowników i zarządzania systemem.

## Usage
Podstawowa składnia polecenia `who` jest następująca:

```csh
who [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `who`:

- `-b`: Wyświetla czas ostatniego uruchomienia systemu.
- `-q`: Wyświetla tylko listę użytkowników oraz ich liczbę.
- `-H`: Wyświetla nagłówki kolumn w wynikach.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `who`:

1. Aby wyświetlić listę wszystkich zalogowanych użytkowników:
   ```csh
   who
   ```

2. Aby zobaczyć czas ostatniego uruchomienia systemu:
   ```csh
   who -b
   ```

3. Aby wyświetlić tylko użytkowników i ich liczbę:
   ```csh
   who -q
   ```

4. Aby wyświetlić listę użytkowników z nagłówkami kolumn:
   ```csh
   who -H
   ```

## Tips
- Używaj opcji `-q`, gdy chcesz szybko sprawdzić, ilu użytkowników jest zalogowanych, bez przeglądania pełnej listy.
- Regularne monitorowanie zalogowanych użytkowników może pomóc w identyfikacji nieautoryzowanych sesji.
- Możesz łączyć `who` z innymi poleceniami, aby uzyskać bardziej szczegółowe informacje, na przykład używając `grep`, aby filtrować wyniki.