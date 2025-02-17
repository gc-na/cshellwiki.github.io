# [Linux] Bash dig użycie: Narzędzie do zapytań DNS

## Overview
Polecenie `dig` (Domain Information Groper) jest używane do wykonywania zapytań DNS. Umożliwia użytkownikom uzyskiwanie informacji o rekordach DNS, co jest przydatne w diagnostyce problemów z siecią oraz w zarządzaniu domenami.

## Usage
Podstawowa składnia polecenia `dig` wygląda następująco:

```bash
dig [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `dig`:

- `@serwer` - Określa serwer DNS, do którego wysyłane jest zapytanie.
- `-t typ` - Umożliwia określenie typu rekordu DNS, np. A, AAAA, MX.
- `+short` - Zwraca skróconą wersję odpowiedzi, co ułatwia odczytanie wyników.
- `-x adres` - Wykonuje odwrotne zapytanie DNS, przekształcając adres IP na nazwę domeny.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `dig`:

1. **Podstawowe zapytanie o rekord A:**
   ```bash
   dig example.com
   ```

2. **Zapytanie o rekord MX dla domeny:**
   ```bash
   dig -t MX example.com
   ```

3. **Użycie konkretnego serwera DNS:**
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Odwrotne zapytanie DNS:**
   ```bash
   dig -x 8.8.8.8
   ```

5. **Skrócona odpowiedź:**
   ```bash
   dig +short example.com
   ```

## Tips
- Używaj opcji `+trace`, aby zobaczyć, jak zapytanie przechodzi przez hierarchię serwerów DNS.
- Zapisuj wyniki zapytań do pliku, aby móc je później analizować.
- Regularnie sprawdzaj rekordy DNS swoich domen, aby upewnić się, że są aktualne i poprawne.