# [Linux] C Shell (csh) traceroute6 użycie: śledzenie trasy pakietów IPv6

## Overview
Polecenie `traceroute6` służy do śledzenia trasy pakietów w sieci IPv6. Umożliwia użytkownikom zrozumienie, przez jakie węzły przechodzą dane, zanim dotrą do docelowego adresu IP. Jest to przydatne narzędzie do diagnozowania problemów z łącznością i analizowania wydajności sieci.

## Usage
Podstawowa składnia polecenia `traceroute6` jest następująca:

```bash
traceroute6 [opcje] [argumenty]
```

## Common Options
- `-m <max_ttl>`: Ustala maksymalny czas życia (TTL) pakietu.
- `-n`: Nie rozwiązuje adresów IP na nazwy hostów, co przyspiesza działanie.
- `-p <port>`: Ustala port, który ma być używany do wysyłania pakietów.
- `-q <nqueries>`: Ustala liczbę zapytań wysyłanych do każdego węzła.

## Common Examples
1. **Podstawowe użycie**:
   Śledzenie trasy do adresu IPv6:
   ```bash
   traceroute6 2001:db8::1
   ```

2. **Użycie z maksymalnym TTL**:
   Ustalenie maksymalnego TTL na 30:
   ```bash
   traceroute6 -m 30 2001:db8::1
   ```

3. **Bez rozwiązywania nazw**:
   Śledzenie trasy bez rozwiązywania adresów IP:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

4. **Użycie z określonym portem**:
   Śledzenie trasy z użyciem portu 80:
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

## Tips
- Używaj opcji `-n`, aby przyspieszyć działanie, gdy nie potrzebujesz nazw hostów.
- Zwiększ wartość TTL, jeśli nie możesz dotrzeć do dalszych węzłów.
- Regularnie monitoruj trasy do kluczowych serwerów, aby zidentyfikować potencjalne problemy z łącznością.