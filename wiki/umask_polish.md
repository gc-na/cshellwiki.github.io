# [Linux] C Shell (csh) umask użycie: Ustawianie domyślnych uprawnień plików

## Overview
Polecenie `umask` w powłoce C Shell (csh) służy do ustawiania domyślnych uprawnień dla nowych plików i katalogów. Umask określa, które uprawnienia będą usuwane z domyślnych uprawnień, co pozwala na kontrolowanie dostępu do tworzonych zasobów.

## Usage
Podstawowa składnia polecenia `umask` jest następująca:

```csh
umask [opcje] [argumenty]
```

## Common Options
- `-S` - Wyświetla umask w formacie symbolicznym.
- `-p` - Wyświetla aktualną wartość umask bez jej zmiany.

## Common Examples
1. **Wyświetlenie aktualnej wartości umask:**
   ```csh
   umask
   ```

2. **Ustawienie umask na 022, co pozwala na odczyt dla grupy i innych użytkowników:**
   ```csh
   umask 022
   ```

3. **Ustawienie umask na 007, co pozwala na pełne uprawnienia dla właściciela i grupy, ale żadnych dla innych:**
   ```csh
   umask 007
   ```

4. **Wyświetlenie umask w formacie symbolicznym:**
   ```csh
   umask -S
   ```

## Tips
- Ustaw umask na wartość, która odpowiada twoim potrzebom bezpieczeństwa, aby ograniczyć dostęp do plików.
- Regularnie sprawdzaj wartość umask, aby upewnić się, że nie zmieniła się niezamierzenie.
- Możesz dodać polecenie umask do swojego pliku konfiguracyjnego powłoki, aby automatycznie ustawiać preferowane uprawnienia przy każdym uruchomieniu terminala.