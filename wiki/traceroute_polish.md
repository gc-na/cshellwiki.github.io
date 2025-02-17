# [Linux] Bash traceroute użycie: Śledzenie trasy pakietów sieciowych

## Overview
Polecenie `traceroute` służy do śledzenia trasy, jaką pokonują pakiety danych w sieci IP. Umożliwia zidentyfikowanie wszystkich węzłów (routerów), przez które przechodzą pakiety, co może pomóc w diagnozowaniu problemów z połączeniem sieciowym.

## Usage
Podstawowa składnia polecenia `traceroute` jest następująca:

```bash
traceroute [opcje] [adres docelowy]
```

## Common Options
- `-m <liczba>`: Ustala maksymalną liczbę skoków (hops), które mają być śledzone.
- `-p <port>`: Ustala port UDP, który ma być używany do wysyłania pakietów.
- `-n`: Wyświetla adresy IP zamiast nazw hostów.
- `-w <czas>`: Ustala czas oczekiwania na odpowiedź w sekundach.

## Common Examples
1. Śledzenie trasy do strony internetowej:
   ```bash
   traceroute www.example.com
   ```

2. Ustalanie maksymalnej liczby skoków do 15:
   ```bash
   traceroute -m 15 www.example.com
   ```

3. Używanie portu 80 do śledzenia trasy:
   ```bash
   traceroute -p 80 www.example.com
   ```

4. Wyświetlanie tylko adresów IP:
   ```bash
   traceroute -n www.example.com
   ```

## Tips
- Używaj opcji `-n`, aby przyspieszyć proces, zwłaszcza w przypadku dużych sieci, gdzie rozwiązywanie nazw hostów może być czasochłonne.
- Zwiększ wartość `-m`, jeśli podejrzewasz, że pakiety mogą przechodzić przez wiele węzłów, aby uzyskać pełny obraz trasy.
- Sprawdzaj różne porty, aby zdiagnozować problemy z różnymi usługami sieciowymi.