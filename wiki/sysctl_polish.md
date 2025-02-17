# [Linux] Bash sysctl użycie: Zarządzanie parametrami jądra systemu

## Przegląd
Polecenie `sysctl` służy do wyświetlania i modyfikowania parametrów jądra systemu w czasie rzeczywistym. Umożliwia administratorom systemu dostosowanie ustawień systemowych bez konieczności ponownego uruchamiania systemu.

## Użycie
Podstawowa składnia polecenia `sysctl` jest następująca:

```bash
sysctl [opcje] [argumenty]
```

## Częste opcje
- `-a`: Wyświetla wszystkie dostępne parametry jądra.
- `-n`: Wyświetla wartość parametru bez jego nazwy.
- `-w`: Umożliwia zmianę wartości parametru.
- `-p`: Wczytuje parametry z pliku konfiguracyjnego.

## Częste przykłady
1. **Wyświetlenie wszystkich parametrów jądra:**
   ```bash
   sysctl -a
   ```

2. **Sprawdzenie konkretnego parametru:**
   ```bash
   sysctl vm.swappiness
   ```

3. **Zmiana wartości parametru:**
   ```bash
   sysctl -w vm.swappiness=10
   ```

4. **Wczytanie parametrów z pliku konfiguracyjnego:**
   ```bash
   sysctl -p
   ```

5. **Wyświetlenie wartości parametru bez jego nazwy:**
   ```bash
   sysctl -n net.ipv4.ip_forward
   ```

## Wskazówki
- Zawsze sprawdzaj aktualne wartości parametrów przed ich zmianą, aby uniknąć niepożądanych efektów.
- Używaj opcji `-p`, aby wczytać zmiany z pliku konfiguracyjnego po edytowaniu, co ułatwia zarządzanie ustawieniami.
- Pamiętaj, że niektóre zmiany mogą wymagać uprawnień administratora, dlatego używaj `sudo`, gdy to konieczne.