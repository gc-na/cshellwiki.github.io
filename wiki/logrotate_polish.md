# [Linux] C Shell (csh) logrotate użycie: Zarządzanie rotacją plików dziennika

## Przegląd
Polecenie `logrotate` służy do zarządzania rotacją plików dziennika w systemach Unix i Linux. Umożliwia automatyczne archiwizowanie, usuwanie lub kompresowanie plików dziennika, co pomaga w utrzymaniu porządku i oszczędzaniu miejsca na dysku.

## Użycie
Podstawowa składnia polecenia `logrotate` jest następująca:

```bash
logrotate [opcje] [argumenty]
```

## Częste opcje
- `-f` : Wymusza rotację plików dziennika, niezależnie od ustawień.
- `-s` : Określa plik stanu, który przechowuje informacje o rotacji.
- `-v` : Włącza tryb szczegółowy, wyświetlając więcej informacji podczas działania.
- `-d` : Uruchamia w trybie debugowania, bez rzeczywistej rotacji.

## Częste przykłady
1. **Podstawowe użycie z domyślnym plikiem konfiguracyjnym:**
   ```bash
   logrotate /etc/logrotate.conf
   ```

2. **Wymuszenie rotacji pliku dziennika:**
   ```bash
   logrotate -f /etc/logrotate.conf
   ```

3. **Uruchomienie w trybie szczegółowym:**
   ```bash
   logrotate -v /etc/logrotate.conf
   ```

4. **Użycie pliku stanu:**
   ```bash
   logrotate -s /var/lib/logrotate/status /etc/logrotate.conf
   ```

## Wskazówki
- Regularnie sprawdzaj plik konfiguracyjny `logrotate`, aby upewnić się, że wszystkie pliki dziennika są prawidłowo skonfigurowane.
- Używaj opcji `-d` przed rzeczywistym uruchomieniem, aby zobaczyć, co zostanie zrobione bez wprowadzania zmian.
- Rozważ użycie kompresji dla starszych plików dziennika, aby zaoszczędzić miejsce na dysku.