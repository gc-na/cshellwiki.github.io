# [Linux] C Shell (csh) dig użycie: narzędzie do zapytań DNS

## Overview
Polecenie `dig` (Domain Information Groper) jest używane do wykonywania zapytań DNS. Umożliwia użytkownikom uzyskiwanie informacji o rekordach DNS, takich jak adresy IP, rekordy MX i inne.

## Usage
Podstawowa składnia polecenia `dig` jest następująca:

```csh
dig [opcje] [argumenty]
```

## Common Options
- `@serwer` - Określa serwer DNS, do którego wysyłane jest zapytanie.
- `-t typ` - Określa typ rekordu DNS, który ma być wyszukiwany (np. A, MX, CNAME).
- `+short` - Zwraca krótką odpowiedź, bez dodatkowych informacji.
- `+trace` - Śledzi zapytanie przez wszystkie serwery DNS.

## Common Examples
- Aby uzyskać adres IP dla domeny:
  ```csh
  dig example.com
  ```

- Aby uzyskać rekord MX dla domeny:
  ```csh
  dig -t MX example.com
  ```

- Aby zapytać konkretny serwer DNS:
  ```csh
  dig @8.8.8.8 example.com
  ```

- Aby uzyskać krótką odpowiedź:
  ```csh
  dig +short example.com
  ```

- Aby śledzić zapytanie przez wszystkie serwery DNS:
  ```csh
  dig +trace example.com
  ```

## Tips
- Używaj opcji `+short`, aby szybko uzyskać tylko najważniejsze informacje.
- Zawsze określaj serwer DNS, jeśli chcesz uzyskać wyniki z konkretnego źródła.
- Eksperymentuj z różnymi typami rekordów, aby lepiej zrozumieć, jakie informacje są dostępne dla danej domeny.