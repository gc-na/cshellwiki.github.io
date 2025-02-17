# [Linux] Bash nslookup użycie: Sprawdzanie adresów IP i nazw domen

## Overview
Polecenie `nslookup` służy do zapytania serwerów DNS w celu uzyskania informacji o adresach IP oraz nazwach domen. Umożliwia to użytkownikom diagnozowanie problemów z DNS oraz weryfikację, czy konkretne nazwy domen są poprawnie rozwiązywane.

## Usage
Podstawowa składnia polecenia `nslookup` jest następująca:

```bash
nslookup [opcje] [argumenty]
```

## Common Options
- `-type=TYPE`: Określa typ zapytania, na przykład A (adres IPv4), AAAA (adres IPv6), MX (rekordy poczty).
- `-timeout=SEC`: Ustawia czas oczekiwania na odpowiedź w sekundach.
- `-retry=N`: Określa liczbę prób ponownego zapytania, jeśli nie otrzymano odpowiedzi.
- `-debug`: Włącza tryb debugowania, co pozwala na uzyskanie szczegółowych informacji o zapytaniach.

## Common Examples
1. **Sprawdzanie adresu IP dla nazwy domeny:**
   ```bash
   nslookup example.com
   ```

2. **Sprawdzanie rekordów MX dla domeny:**
   ```bash
   nslookup -type=MX example.com
   ```

3. **Użycie konkretnego serwera DNS:**
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. **Sprawdzanie rekordu AAAA (adres IPv6):**
   ```bash
   nslookup -type=AAAA example.com
   ```

## Tips
- Używaj opcji `-debug`, aby uzyskać więcej informacji podczas rozwiązywania problemów z DNS.
- Zawsze sprawdzaj różne serwery DNS, aby upewnić się, że problem nie leży po stronie lokalnego serwera.
- Pamiętaj, że wyniki mogą się różnić w zależności od serwera DNS, którego używasz.