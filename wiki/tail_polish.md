# [Linux] Bash tail użycie: Wyświetlanie końca pliku

## Overview
Polecenie `tail` w systemie Linux służy do wyświetlania ostatnich linii pliku tekstowego. Jest to przydatne narzędzie do monitorowania logów lub plików, które są regularnie aktualizowane.

## Usage
Podstawowa składnia polecenia `tail` wygląda następująco:

```bash
tail [opcje] [argumenty]
```

## Common Options
- `-n NUM` – Wyświetla ostatnie NUM linii z pliku. Na przykład `-n 10` pokaże ostatnie 10 linii.
- `-f` – Śledzi plik w czasie rzeczywistym, wyświetlając nowe linie, gdy są dodawane.
- `-c NUM` – Wyświetla ostatnie NUM bajtów z pliku.
- `-q` – Wyłącza nagłówki plików, gdy wyświetlane są wiele plików.

## Common Examples
1. Wyświetlenie ostatnich 10 linii pliku:
   ```bash
   tail /var/log/syslog
   ```

2. Wyświetlenie ostatnich 20 linii pliku:
   ```bash
   tail -n 20 /var/log/syslog
   ```

3. Śledzenie pliku w czasie rzeczywistym:
   ```bash
   tail -f /var/log/syslog
   ```

4. Wyświetlenie ostatnich 100 bajtów z pliku:
   ```bash
   tail -c 100 /var/log/syslog
   ```

5. Wyświetlenie ostatnich 5 linii z kilku plików:
   ```bash
   tail -n 5 plik1.txt plik2.txt
   ```

## Tips
- Używaj opcji `-f`, aby monitorować pliki logów w czasie rzeczywistym, co jest szczególnie przydatne podczas debugowania.
- Możesz łączyć `tail` z innymi poleceniami, takimi jak `grep`, aby filtrować wyniki. Na przykład:
  ```bash
  tail -f /var/log/syslog | grep "error"
  ```
- Pamiętaj, że `tail` działa najlepiej z plikami tekstowymi. Używanie go z plikami binarnymi może dać nieprzewidywalne wyniki.