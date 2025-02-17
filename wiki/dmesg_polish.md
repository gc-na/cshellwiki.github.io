# [Linux] Bash dmesg użycie: Wyświetlanie komunikatów jądra

## Overview
Polecenie `dmesg` służy do wyświetlania komunikatów jądra systemu operacyjnego, które są generowane podczas uruchamiania systemu oraz w trakcie jego działania. Umożliwia to użytkownikom i administratorom monitorowanie zdarzeń systemowych, diagnozowanie problemów oraz analizowanie działania sprzętu.

## Usage
Podstawowa składnia polecenia `dmesg` jest następująca:

```bash
dmesg [opcje] [argumenty]
```

## Common Options
- `-C` – Wyczyść bufor komunikatów jądra.
- `-c` – Wyświetl komunikaty i następnie je wyczyść.
- `-n level` – Ustaw poziom logowania komunikatów.
- `-T` – Wyświetl czas w formacie czytelnym dla ludzi.
- `-f facility` – Filtruj komunikaty według określonej jednostki (np. kern, user).

## Common Examples
1. **Wyświetlenie wszystkich komunikatów jądra:**
   ```bash
   dmesg
   ```

2. **Wyświetlenie komunikatów z czytelnym czasem:**
   ```bash
   dmesg -T
   ```

3. **Wyczyść bufor komunikatów jądra:**
   ```bash
   dmesg -C
   ```

4. **Filtracja komunikatów według jednostki:**
   ```bash
   dmesg -f user
   ```

5. **Ustawienie poziomu logowania:**
   ```bash
   dmesg -n 1
   ```

## Tips
- Używaj opcji `-T`, aby łatwiej interpretować czasy komunikatów.
- Regularnie sprawdzaj komunikaty jądra po aktualizacji sprzętu lub oprogramowania, aby szybko wychwycić potencjalne problemy.
- Możesz użyć potoku (pipe) z `grep`, aby wyszukiwać konkretne komunikaty, co ułatwia analizę:
  ```bash
  dmesg | grep error
  ```