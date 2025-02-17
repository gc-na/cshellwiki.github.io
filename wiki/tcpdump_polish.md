# [Linux] Bash tcpdump użycie: Analiza ruchu sieciowego

## Overview
Polecenie `tcpdump` jest narzędziem do przechwytywania i analizy pakietów przesyłanych w sieci. Umożliwia monitorowanie ruchu sieciowego w czasie rzeczywistym oraz zapisywanie danych do późniejszej analizy. Jest to niezwykle przydatne narzędzie dla administratorów systemów i specjalistów ds. bezpieczeństwa.

## Usage
Podstawowa składnia polecenia `tcpdump` jest następująca:

```bash
tcpdump [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `tcpdump`:

- `-i <interfejs>`: Określa interfejs sieciowy, z którego mają być przechwytywane pakiety.
- `-w <plik>`: Zapisuje przechwycone pakiety do pliku.
- `-r <plik>`: Odczytuje pakiety z pliku.
- `-c <liczba>`: Przechwytuje określoną liczbę pakietów.
- `-n`: Nie przekształca adresów IP na nazwy hostów.
- `-v`, `-vv`, `-vvv`: Zwiększa szczegółowość wyjścia.

## Common Examples

1. **Przechwytywanie pakietów na domyślnym interfejsie:**
   ```bash
   tcpdump
   ```

2. **Przechwytywanie pakietów na określonym interfejsie:**
   ```bash
   tcpdump -i eth0
   ```

3. **Zapis przechwyconych pakietów do pliku:**
   ```bash
   tcpdump -w ruch.pcap
   ```

4. **Odczyt pakietów z pliku:**
   ```bash
   tcpdump -r ruch.pcap
   ```

5. **Przechwytywanie tylko 10 pakietów:**
   ```bash
   tcpdump -c 10
   ```

6. **Przechwytywanie pakietów bez rozwiązywania nazw:**
   ```bash
   tcpdump -n
   ```

## Tips
- Używaj opcji `-i` do wskazania konkretnego interfejsu, aby uniknąć przechwytywania niepotrzebnych danych.
- Zapisuj przechwycone pakiety do pliku, aby móc je później analizować w narzędziach takich jak Wireshark.
- Regularnie korzystaj z opcji `-v`, aby uzyskać więcej informacji o pakietach, co może pomóc w diagnozowaniu problemów.
- Pamiętaj, że do używania `tcpdump` mogą być wymagane uprawnienia administratora, dlatego warto uruchamiać polecenie z `sudo`, jeśli to konieczne.