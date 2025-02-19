# [Linux] C Shell (csh) free użycie: wyświetlanie informacji o pamięci

## Overview
Polecenie `free` w systemie Linux służy do wyświetlania informacji o pamięci systemowej, w tym pamięci RAM oraz pamięci wymiany (swap). Umożliwia to użytkownikom monitorowanie wykorzystania pamięci w systemie.

## Usage
Podstawowa składnia polecenia `free` jest następująca:

```csh
free [options] [arguments]
```

## Common Options
- `-h` – wyświetla wartości w formacie czytelnym dla człowieka (np. MB, GB).
- `-m` – wyświetla wartości w megabajtach.
- `-g` – wyświetla wartości w gigabajtach.
- `-s [sekundy]` – aktualizuje wyjście co określoną liczbę sekund.

## Common Examples
1. Wyświetlenie podstawowych informacji o pamięci:
   ```csh
   free
   ```

2. Wyświetlenie informacji o pamięci w formacie czytelnym dla człowieka:
   ```csh
   free -h
   ```

3. Wyświetlenie informacji o pamięci w megabajtach:
   ```csh
   free -m
   ```

4. Wyświetlenie informacji o pamięci co 5 sekund:
   ```csh
   free -s 5
   ```

## Tips
- Używaj opcji `-h`, aby łatwiej zrozumieć, ile pamięci jest dostępne i używane.
- Regularne monitorowanie pamięci może pomóc w identyfikacji problemów z wydajnością systemu.
- Możesz połączyć `free` z innymi poleceniami, takimi jak `watch`, aby na bieżąco obserwować zmiany w pamięci:
   ```csh
   watch free -h
   ```