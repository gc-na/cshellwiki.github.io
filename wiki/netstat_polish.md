# [Systemy Unixowe] C Shell (csh) netstat Użycie: Wyświetlanie informacji o połączeniach sieciowych

## Przegląd
Polecenie `netstat` służy do wyświetlania informacji o połączeniach sieciowych, trasach, statystykach interfejsów oraz innych danych związanych z siecią. Jest to przydatne narzędzie do monitorowania aktywności sieciowej oraz diagnozowania problemów.

## Użycie
Podstawowa składnia polecenia `netstat` jest następująca:

```
netstat [opcje] [argumenty]
```

## Często używane opcje
- `-a`: Wyświetla wszystkie połączenia i porty nasłuchujące.
- `-n`: Wyświetla adresy IP i numery portów w formie numerycznej, bez rozwiązywania nazw.
- `-r`: Wyświetla tablicę routingu.
- `-i`: Wyświetla statystyki interfejsów sieciowych.
- `-s`: Wyświetla statystyki protokołów.

## Częste przykłady
1. Wyświetlenie wszystkich aktywnych połączeń:
   ```csh
   netstat -a
   ```

2. Wyświetlenie połączeń z adresami IP w formie numerycznej:
   ```csh
   netstat -an
   ```

3. Wyświetlenie tablicy routingu:
   ```csh
   netstat -r
   ```

4. Wyświetlenie statystyk interfejsów sieciowych:
   ```csh
   netstat -i
   ```

5. Wyświetlenie statystyk protokołów:
   ```csh
   netstat -s
   ```

## Wskazówki
- Używaj opcji `-n`, aby przyspieszyć wyświetlanie wyników, unikając rozwiązywania nazw.
- Regularnie monitoruj połączenia, aby szybko wykrywać nieautoryzowane aktywności.
- Łącz różne opcje, aby uzyskać bardziej szczegółowe informacje, np. `netstat -anr`, aby zobaczyć połączenia i tablicę routingu jednocześnie.