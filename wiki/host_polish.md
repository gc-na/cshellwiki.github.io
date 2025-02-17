# [Linux] Bash host użycie: narzędzie do zapytań DNS

## Overview
Polecenie `host` jest używane do wykonywania zapytań DNS (Domain Name System). Umożliwia użytkownikom przekształcanie nazw domen na adresy IP oraz odwrotnie, co jest przydatne w diagnostyce i zarządzaniu sieciami.

## Usage
Podstawowa składnia polecenia `host` jest następująca:

```bash
host [opcje] [argumenty]
```

## Common Options
- `-a`: Wyświetla wszystkie dostępne informacje o danej nazwie.
- `-t TYPE`: Określa typ rekordu DNS do zapytania (np. A, MX, CNAME).
- `-v`: Włącza tryb szczegółowy, co pozwala na uzyskanie dodatkowych informacji o zapytaniu.
- `-W TIMEOUT`: Ustala limit czasu na odpowiedź w sekundach.

## Common Examples
1. **Znalezienie adresu IP dla nazwy domeny:**
   ```bash
   host example.com
   ```

2. **Znalezienie rekordu MX dla domeny:**
   ```bash
   host -t MX example.com
   ```

3. **Znalezienie wszystkich informacji o domenie:**
   ```bash
   host -a example.com
   ```

4. **Znalezienie adresu IP dla subdomeny:**
   ```bash
   host sub.example.com
   ```

5. **Użycie z określonym serwerem DNS:**
   ```bash
   host example.com 8.8.8.8
   ```

## Tips
- Używaj opcji `-v`, aby uzyskać więcej informacji o zapytaniach, co może być pomocne w rozwiązywaniu problemów.
- Sprawdzaj różne typy rekordów DNS, aby uzyskać pełniejszy obraz konfiguracji domeny.
- Pamiętaj, że niektóre rekordy mogą być cache'owane, więc wyniki mogą się różnić w zależności od używanego serwera DNS.