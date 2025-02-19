# [Linux] C Shell (csh) tail użycie: wyświetlanie końca plików

## Przegląd
Polecenie `tail` służy do wyświetlania ostatnich linii pliku tekstowego. Jest to przydatne narzędzie do monitorowania logów lub plików, które są regularnie aktualizowane.

## Użycie
Podstawowa składnia polecenia `tail` jest następująca:

```csh
tail [opcje] [argumenty]
```

## Częste opcje
- `-n [liczba]`: Wyświetla ostatnie `liczba` linii pliku.
- `-f`: Śledzi zmiany w pliku w czasie rzeczywistym, wyświetlając nowe linie, gdy są dodawane.
- `-c [liczba]`: Wyświetla ostatnie `liczba` bajtów pliku.

## Przykłady
1. Wyświetlenie ostatnich 10 linii pliku `log.txt`:
   ```csh
   tail log.txt
   ```

2. Wyświetlenie ostatnich 20 linii pliku `data.txt`:
   ```csh
   tail -n 20 data.txt
   ```

3. Śledzenie pliku `server.log` w czasie rzeczywistym:
   ```csh
   tail -f server.log
   ```

4. Wyświetlenie ostatnich 50 bajtów pliku `output.txt`:
   ```csh
   tail -c 50 output.txt
   ```

## Wskazówki
- Używaj opcji `-f`, gdy chcesz monitorować plik logów na żywo, co jest szczególnie przydatne w przypadku aplikacji serwerowych.
- Możesz łączyć `tail` z innymi poleceniami, takimi jak `grep`, aby filtrować wyniki. Na przykład:
  ```csh
  tail -f server.log | grep "ERROR"
  ```
- Pamiętaj, że `tail` domyślnie wyświetla 10 ostatnich linii, co może być wystarczające w wielu przypadkach.