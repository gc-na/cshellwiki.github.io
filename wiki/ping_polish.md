# [Linux] Bash ping użycie: Sprawdzanie dostępności hosta

## Overview
Polecenie `ping` jest używane do sprawdzania dostępności hostów w sieci. Wysyła pakiety ICMP Echo Request do określonego adresu IP lub nazwy hosta i oczekuje na odpowiedzi, co pozwala na ocenę, czy dany host jest osiągalny oraz na pomiar czasu odpowiedzi.

## Usage
Podstawowa składnia polecenia `ping` wygląda następująco:

```bash
ping [opcje] [argumenty]
```

## Common Options
- `-c [liczba]`: Określa liczbę wysyłanych pakietów.
- `-i [czas]`: Ustala czas w sekundach pomiędzy wysyłanymi pakietami.
- `-t [TTL]`: Ustala wartość TTL (Time To Live) dla pakietów.
- `-s [rozmiar]`: Ustala rozmiar wysyłanych pakietów w bajtach.
- `-W [czas]`: Ustala czas oczekiwania na odpowiedź w sekundach.

## Common Examples
1. **Sprawdzenie dostępności hosta:**
   ```bash
   ping google.com
   ```

2. **Wysłanie 5 pakietów do hosta:**
   ```bash
   ping -c 5 google.com
   ```

3. **Ustalenie interwału 2 sekundy pomiędzy pakietami:**
   ```bash
   ping -i 2 google.com
   ```

4. **Sprawdzenie dostępności lokalnego hosta:**
   ```bash
   ping 127.0.0.1
   ```

5. **Ustalenie rozmiaru pakietu na 100 bajtów:**
   ```bash
   ping -s 100 google.com
   ```

## Tips
- Używaj opcji `-c`, aby uniknąć nieskończonego wysyłania pakietów, co jest szczególnie przydatne w skryptach.
- Monitoruj czas odpowiedzi, aby ocenić wydajność połączenia.
- Używaj `ping` do diagnozowania problemów z siecią, sprawdzając, czy pakiety są tracone.