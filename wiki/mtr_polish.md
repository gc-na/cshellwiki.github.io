# [Linux] Bash mtr Użycie: narzędzie do diagnostyki sieci

## Overview
Polecenie `mtr` (My Traceroute) łączy funkcje polecenia `traceroute` i `ping`, umożliwiając użytkownikom monitorowanie i analizowanie tras pakietów w sieci. Dzięki `mtr` można uzyskać informacje o opóźnieniach i utracie pakietów na każdym hopie w trasie do docelowego adresu IP.

## Usage
Podstawowa składnia polecenia `mtr` jest następująca:

```bash
mtr [opcje] [adres]
```

## Common Options
- `-r`: Generuje raport w trybie tekstowym.
- `-c [liczba]`: Określa liczbę wysyłanych pakietów.
- `-i [czas]`: Ustala czas między wysyłanymi pakietami (w sekundach).
- `-p`: Uruchamia `mtr` w trybie monitorowania, co pozwala na ciągłe wyświetlanie wyników.

## Common Examples
1. **Podstawowe użycie**:
   ```bash
   mtr google.com
   ```

2. **Raport w trybie tekstowym**:
   ```bash
   mtr -r google.com
   ```

3. **Określenie liczby pakietów**:
   ```bash
   mtr -c 10 google.com
   ```

4. **Monitorowanie z określonym czasem między pakietami**:
   ```bash
   mtr -i 1 google.com
   ```

## Tips
- Używaj opcji `-r`, aby uzyskać zwięzły raport, który można łatwo zapisać lub udostępnić.
- Regularne monitorowanie tras do kluczowych serwerów może pomóc w szybkim wykrywaniu problemów z siecią.
- W przypadku problemów z połączeniem, porównaj wyniki `mtr` z wynikami `ping` i `traceroute`, aby uzyskać pełniejszy obraz sytuacji.