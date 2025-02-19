# [Linux] C Shell (csh) ping użycie: Sprawdzanie dostępności hostów w sieci

## Overview
Polecenie `ping` służy do sprawdzania dostępności hostów w sieci poprzez wysyłanie pakietów ICMP Echo Request i oczekiwanie na odpowiedzi. Jest to przydatne narzędzie do diagnozowania problemów z połączeniem sieciowym.

## Usage
Podstawowa składnia polecenia `ping` wygląda następująco:

```csh
ping [opcje] [argumenty]
```

## Common Options
- `-c <liczba>`: Określa liczbę wysyłanych pakietów.
- `-i <czas>`: Ustala czas w sekundach pomiędzy wysyłanymi pakietami.
- `-s <rozmiar>`: Ustala rozmiar wysyłanych pakietów.
- `-t <czas>`: Ustala czas życia pakietu (TTL).

## Common Examples
1. Sprawdzenie dostępności hosta:
   ```csh
   ping example.com
   ```

2. Wysłanie 5 pakietów:
   ```csh
   ping -c 5 example.com
   ```

3. Ustalenie interwału 2 sekund pomiędzy pakietami:
   ```csh
   ping -i 2 example.com
   ```

4. Wysłanie pakietów o rozmiarze 128 bajtów:
   ```csh
   ping -s 128 example.com
   ```

5. Ustalenie czasu życia pakietu na 64:
   ```csh
   ping -t 64 example.com
   ```

## Tips
- Używaj opcji `-c`, aby ograniczyć liczbę wysyłanych pakietów, co jest przydatne w przypadku testów.
- Monitoruj czas odpowiedzi, aby ocenić jakość połączenia.
- Jeśli ping nie działa, sprawdź, czy host jest dostępny i czy nie ma problemów z konfiguracją sieci.