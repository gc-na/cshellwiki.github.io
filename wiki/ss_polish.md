# [Linux] Bash ss użycie: Narzędzie do monitorowania gniazd sieciowych

## Overview
Polecenie `ss` (socket statistics) jest używane do wyświetlania informacji o gniazdach sieciowych w systemie Linux. Umożliwia ono monitorowanie połączeń TCP, UDP oraz innych typów gniazd, co czyni je przydatnym narzędziem do diagnostyki sieci.

## Usage
Podstawowa składnia polecenia `ss` jest następująca:

```bash
ss [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `ss`:

- `-t`: Wyświetla tylko połączenia TCP.
- `-u`: Wyświetla tylko połączenia UDP.
- `-l`: Pokazuje tylko gniazda nasłuchujące.
- `-p`: Wyświetla procesy powiązane z gniazdami.
- `-n`: Wyświetla numery portów i adresy IP w formie numerycznej, zamiast rozwiązywać je na nazwy.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `ss`:

1. Wyświetlenie wszystkich aktywnych połączeń TCP:
   ```bash
   ss -t
   ```

2. Wyświetlenie wszystkich gniazd nasłuchujących:
   ```bash
   ss -l
   ```

3. Wyświetlenie połączeń UDP:
   ```bash
   ss -u
   ```

4. Wyświetlenie gniazd z informacjami o procesach:
   ```bash
   ss -p
   ```

5. Wyświetlenie wszystkich połączeń z adresami IP w formie numerycznej:
   ```bash
   ss -n
   ```

## Tips
- Używaj opcji `-t` i `-u` razem, aby uzyskać pełny obraz połączeń TCP i UDP:
  ```bash
  ss -tu
  ```
- Regularne monitorowanie gniazd sieciowych może pomóc w identyfikacji problemów z połączeniami.
- Zapisuj wyniki polecenia do pliku, aby móc je później analizować:
  ```bash
  ss -t > gniazda.txt
  ```