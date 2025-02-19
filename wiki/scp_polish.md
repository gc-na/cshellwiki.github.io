# [Linux] C Shell (csh) scp użycie: Kopiowanie plików między hostami

## Overview
Polecenie `scp` (secure copy) służy do bezpiecznego kopiowania plików między różnymi hostami w sieci. Wykorzystuje protokół SSH do zapewnienia szyfrowania danych podczas transferu.

## Usage
Podstawowa składnia polecenia `scp` jest następująca:

```csh
scp [opcje] [źródło] [cel]
```

## Common Options
- `-r`: Kopiuje katalogi rekurencyjnie.
- `-P`: Określa port, jeśli nie jest to domyślny port SSH (22).
- `-i`: Używa określonego klucza prywatnego do uwierzytelnienia.
- `-v`: Włącza tryb szczegółowy, co pozwala na śledzenie postępu transferu.

## Common Examples
1. **Kopiowanie pliku z lokalnego systemu na zdalny serwer:**
   ```csh
   scp lokalny_plik.txt użytkownik@zdalny_serwer:/ścieżka/do/docelowego/
   ```

2. **Kopiowanie pliku ze zdalnego serwera na lokalny system:**
   ```csh
   scp użytkownik@zdalny_serwer:/ścieżka/do/zdalnego_pliku.txt /ścieżka/do/lokalnego/
   ```

3. **Kopiowanie katalogu rekurencyjnie:**
   ```csh
   scp -r lokalny_katalog użytkownik@zdalny_serwer:/ścieżka/do/docelowego/
   ```

4. **Kopiowanie pliku na zdalny serwer z określonym portem:**
   ```csh
   scp -P 2222 lokalny_plik.txt użytkownik@zdalny_serwer:/ścieżka/do/docelowego/
   ```

## Tips
- Używaj opcji `-v`, aby uzyskać więcej informacji o procesie transferu, co może pomóc w diagnozowaniu problemów.
- Zawsze upewnij się, że masz odpowiednie uprawnienia do plików, które chcesz skopiować.
- Rozważ użycie kluczy SSH do uwierzytelnienia, aby uprościć proces logowania i zwiększyć bezpieczeństwo.