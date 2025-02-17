# [Linux] Bash date użycie: Wyświetlanie i formatowanie daty

## Overview
Polecenie `date` w systemie Linux służy do wyświetlania oraz formatowania daty i godziny. Umożliwia użytkownikom uzyskanie aktualnych informacji o czasie oraz dostosowanie ich do różnych formatów.

## Usage
Podstawowa składnia polecenia `date` jest następująca:

```bash
date [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `date`:

- `+FORMAT` - pozwala na określenie formatu wyjścia daty.
- `-u` - wyświetla czas w formacie UTC (czas uniwersalny).
- `-d STRING` - interpretuje podany ciąg jako datę i wyświetla ją.
- `-R` - wyświetla datę w formacie RFC 2822.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `date`:

1. Wyświetlenie aktualnej daty i godziny:
   ```bash
   date
   ```

2. Wyświetlenie daty w formacie YYYY-MM-DD:
   ```bash
   date +%Y-%m-%d
   ```

3. Wyświetlenie daty w formacie pełnym (np. "poniedziałek, 1 stycznia 2023"):
   ```bash
   date +"%A, %d %B %Y"
   ```

4. Wyświetlenie daty w strefie czasowej UTC:
   ```bash
   date -u
   ```

5. Interpretacja podanego ciągu jako daty (np. "2 dni temu"):
   ```bash
   date -d "2 days ago"
   ```

6. Wyświetlenie daty w formacie RFC 2822:
   ```bash
   date -R
   ```

## Tips
- Używaj opcji `+FORMAT`, aby dostosować wyjście do swoich potrzeb, co może być przydatne w skryptach.
- Pamiętaj, że formaty daty są wrażliwe na wielkość liter, więc upewnij się, że używasz odpowiednich symboli.
- Możesz używać polecenia `date` w połączeniu z innymi poleceniami, aby automatycznie dodawać datę do plików lub logów.