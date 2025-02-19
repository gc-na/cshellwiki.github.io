# [Linux] C Shell (csh) ss użycie: wyświetlanie informacji o gniazdach

## Overview
Polecenie `ss` służy do wyświetlania informacji o gniazdach sieciowych w systemie. Umożliwia monitorowanie połączeń, portów oraz stanu gniazd, co jest przydatne w diagnostyce i zarządzaniu siecią.

## Usage
Podstawowa składnia polecenia `ss` jest następująca:

```bash
ss [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `ss`:

- `-t` – wyświetla tylko gniazda TCP.
- `-u` – wyświetla tylko gniazda UDP.
- `-l` – pokazuje tylko gniazda nasłuchujące.
- `-p` – wyświetla procesy powiązane z gniazdami.
- `-n` – pokazuje numery portów zamiast nazw usług.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `ss`:

1. Wyświetlenie wszystkich gniazd TCP:
   ```bash
   ss -t
   ```

2. Wyświetlenie wszystkich gniazd UDP:
   ```bash
   ss -u
   ```

3. Wyświetlenie gniazd nasłuchujących:
   ```bash
   ss -l
   ```

4. Wyświetlenie gniazd z informacjami o procesach:
   ```bash
   ss -p
   ```

5. Wyświetlenie gniazd z numerami portów:
   ```bash
   ss -n
   ```

## Tips
- Używaj opcji `-p`, aby zidentyfikować procesy korzystające z gniazd, co może pomóc w diagnostyce problemów z siecią.
- Kombinuj różne opcje, aby uzyskać bardziej szczegółowe informacje, na przykład `ss -tunlp`, aby zobaczyć zarówno TCP, jak i UDP z informacjami o procesach.
- Regularnie monitoruj gniazda, aby szybko reagować na nieautoryzowane połączenia lub problemy z siecią.