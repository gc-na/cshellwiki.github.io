# [Linux] Bash ping6 użycie: Sprawdzanie dostępności hostów w sieci IPv6

## Overview
Polecenie `ping6` służy do sprawdzania dostępności hostów w sieci IPv6. Umożliwia wysyłanie pakietów ICMP Echo Request do określonego adresu IPv6 i oczekiwanie na odpowiedzi, co pozwala na diagnozowanie problemów z połączeniem sieciowym.

## Usage
Podstawowa składnia polecenia `ping6` wygląda następująco:

```bash
ping6 [opcje] [adres IPv6]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `ping6`:

- `-c [liczba]` - Określa liczbę pakietów do wysłania.
- `-i [czas]` - Ustala czas w sekundach pomiędzy wysyłanymi pakietami.
- `-t [TTL]` - Ustala wartość TTL (Time To Live) dla wysyłanych pakietów.
- `-s [rozmiar]` - Ustala rozmiar wysyłanych pakietów w bajtach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `ping6`:

1. Sprawdzenie dostępności hosta o adresie IPv6:
   ```bash
   ping6 2001:db8::1
   ```

2. Wysłanie 5 pakietów do hosta:
   ```bash
   ping6 -c 5 2001:db8::1
   ```

3. Ustalenie interwału wysyłania pakietów na 2 sekundy:
   ```bash
   ping6 -i 2 2001:db8::1
   ```

4. Wysłanie pakietów o rozmiarze 128 bajtów:
   ```bash
   ping6 -s 128 2001:db8::1
   ```

## Tips
- Używaj opcji `-c`, aby ograniczyć liczbę wysyłanych pakietów, co jest przydatne w testach.
- Sprawdzaj różne adresy IPv6, aby upewnić się, że Twoja sieć działa poprawnie.
- Monitoruj czas odpowiedzi, aby ocenić jakość połączenia z danym hostem.