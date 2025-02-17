# [Linux] Bash traceroute6 użycie: śledzenie tras IPv6

## Overview
Polecenie `traceroute6` służy do śledzenia trasy pakietów w sieciach IPv6. Umożliwia użytkownikom zrozumienie, przez jakie węzły przechodzą dane, zanim dotrą do docelowego adresu IP. To narzędzie jest przydatne w diagnostyce problemów z połączeniami sieciowymi.

## Usage
Podstawowa składnia polecenia `traceroute6` jest następująca:

```bash
traceroute6 [opcje] [adres docelowy]
```

## Common Options
- `-m <liczba>`: Ustala maksymalną liczbę skoków (hops).
- `-p <port>`: Określa port, który ma być używany.
- `-w <czas>`: Ustala czas oczekiwania na odpowiedź w sekundach.
- `-q <liczba>`: Ustala liczbę zapytań wysyłanych do każdego węzła.

## Common Examples
1. **Podstawowe użycie**:
   Śledzenie trasy do adresu IPv6.
   ```bash
   traceroute6 2001:db8::1
   ```

2. **Ustalenie maksymalnej liczby skoków**:
   Śledzenie trasy z maksymalnie 15 skokami.
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. **Użycie określonego portu**:
   Śledzenie trasy do adresu IPv6 na porcie 80.
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. **Zwiększenie liczby zapytań**:
   Wysyłanie 5 zapytań do każdego węzła.
   ```bash
   traceroute6 -q 5 2001:db8::1
   ```

## Tips
- Używaj opcji `-m`, aby uniknąć zbyt długiego śledzenia tras, co może być przydatne w dużych sieciach.
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do wykonywania polecenia, ponieważ niektóre sieci mogą blokować zapytania traceroute.
- Analizuj wyniki, aby zidentyfikować potencjalne problemy z połączeniem, takie jak opóźnienia lub utraty pakietów.