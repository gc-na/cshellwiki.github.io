# [Linux] Bash netstat użycie: Wyświetlanie informacji o połączeniach sieciowych

## Overview
Polecenie `netstat` jest używane do wyświetlania informacji o połączeniach sieciowych, tabelach routingu oraz statystykach interfejsów sieciowych. Umożliwia monitorowanie aktywnych połączeń oraz diagnostykę problemów z siecią.

## Usage
Podstawowa składnia polecenia `netstat` jest następująca:

```bash
netstat [opcje] [argumenty]
```

## Common Options
- `-a`: Wyświetla wszystkie połączenia i porty nasłuchujące.
- `-t`: Pokazuje tylko połączenia TCP.
- `-u`: Pokazuje tylko połączenia UDP.
- `-n`: Wyświetla adresy i numery portów w formacie numerycznym, zamiast rozwiązywać je na nazwy.
- `-l`: Wyświetla tylko porty, które są w stanie nasłuchiwania.
- `-p`: Pokazuje identyfikatory procesów (PID) oraz nazwy programów korzystających z połączeń.

## Common Examples

1. Wyświetlenie wszystkich aktywnych połączeń:
   ```bash
   netstat -a
   ```

2. Wyświetlenie tylko połączeń TCP:
   ```bash
   netstat -t
   ```

3. Wyświetlenie połączeń UDP w formacie numerycznym:
   ```bash
   netstat -u -n
   ```

4. Wyświetlenie portów nasłuchujących:
   ```bash
   netstat -l
   ```

5. Wyświetlenie połączeń z identyfikatorami procesów:
   ```bash
   netstat -p
   ```

## Tips
- Używaj opcji `-n`, aby przyspieszyć wyświetlanie wyników, unikając rozwiązywania nazw.
- Regularnie monitoruj połączenia sieciowe, aby szybko identyfikować nieautoryzowane lub podejrzane aktywności.
- Możesz połączyć `netstat` z innymi narzędziami, takimi jak `grep`, aby filtrować wyniki. Na przykład:
  ```bash
  netstat -tuln | grep ':80'
  ```
- Pamiętaj, że w niektórych systemach operacyjnych `netstat` może być zastąpione przez `ss`, które oferuje bardziej szczegółowe informacje.