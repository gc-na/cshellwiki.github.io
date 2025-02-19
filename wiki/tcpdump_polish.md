# [Linux] C Shell (csh) tcpdump użycie: Narzędzie do przechwytywania pakietów sieciowych

## Przegląd
Polecenie `tcpdump` jest narzędziem do przechwytywania i analizy ruchu sieciowego. Umożliwia monitorowanie pakietów przesyłanych przez interfejsy sieciowe, co jest przydatne do diagnozowania problemów z siecią oraz do analizy bezpieczeństwa.

## Użycie
Podstawowa składnia polecenia `tcpdump` jest następująca:

```bash
tcpdump [opcje] [argumenty]
```

## Częste opcje
- `-i <interfejs>`: Określa interfejs sieciowy do monitorowania.
- `-n`: Wyłącza rozwiązywanie nazw hostów, co przyspiesza działanie.
- `-c <liczba>`: Przechwytuje określoną liczbę pakietów.
- `-w <plik>`: Zapisuje przechwycone pakiety do pliku.
- `-r <plik>`: Odczytuje pakiety z pliku.

## Częste przykłady
- Przechwytywanie pakietów na domyślnym interfejsie:
  ```bash
  tcpdump
  ```

- Przechwytywanie pakietów na określonym interfejsie:
  ```bash
  tcpdump -i eth0
  ```

- Przechwytywanie tylko 10 pakietów:
  ```bash
  tcpdump -c 10
  ```

- Zapis przechwyconych pakietów do pliku:
  ```bash
  tcpdump -w pakiety.pcap
  ```

- Odczyt pakietów z pliku:
  ```bash
  tcpdump -r pakiety.pcap
  ```

## Wskazówki
- Używaj opcji `-n`, aby uniknąć opóźnień związanych z rozwiązywaniem nazw hostów.
- Regularnie filtruj przechwytywane pakiety, aby skupić się na interesujących cię danych, na przykład używając `tcp port 80` do monitorowania ruchu HTTP.
- Zapisuj przechwycone pakiety do pliku, aby móc je później analizować za pomocą narzędzi takich jak Wireshark.