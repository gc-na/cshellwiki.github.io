# [Linux] Bash free użycie: wyświetlanie informacji o pamięci

## Overview
Polecenie `free` w systemie Linux służy do wyświetlania informacji o użyciu pamięci w systemie. Pokazuje ilość pamięci fizycznej, pamięci wymiany oraz buforów i pamięci podręcznej, co pozwala na monitorowanie stanu pamięci w czasie rzeczywistym.

## Usage
Podstawowa składnia polecenia `free` wygląda następująco:

```bash
free [opcje]
```

## Common Options
- `-h` – wyświetla wartości w formacie czytelnym dla człowieka (np. MB, GB).
- `-m` – wyświetla wartości w megabajtach.
- `-g` – wyświetla wartości w gigabajtach.
- `-s [sekundy]` – aktualizuje wyjście co określoną liczbę sekund.
- `-t` – pokazuje całkowitą ilość pamięci.

## Common Examples
1. Wyświetlenie podstawowych informacji o pamięci:
   ```bash
   free
   ```

2. Wyświetlenie informacji w formacie czytelnym dla człowieka:
   ```bash
   free -h
   ```

3. Wyświetlenie informacji w megabajtach:
   ```bash
   free -m
   ```

4. Monitorowanie pamięci co 5 sekund:
   ```bash
   free -s 5
   ```

5. Wyświetlenie całkowitej ilości pamięci:
   ```bash
   free -t
   ```

## Tips
- Używaj opcji `-h`, aby łatwiej interpretować wyniki, zwłaszcza na systemach z dużą ilością pamięci.
- Regularne monitorowanie pamięci może pomóc w identyfikacji problemów z wydajnością systemu.
- Możesz użyć polecenia `watch`, aby automatycznie aktualizować wyjście `free`, co może być przydatne w czasie analizy pamięci:
  ```bash
  watch free -h
  ```