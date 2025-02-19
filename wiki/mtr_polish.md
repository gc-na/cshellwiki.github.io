# [Linux] C Shell (csh) mtr użycie: narzędzie do diagnostyki sieci

## Przegląd
Polecenie `mtr` (My Traceroute) jest narzędziem do diagnostyki sieci, które łączy funkcje poleceń `traceroute` i `ping`. Umożliwia użytkownikom monitorowanie trasy pakietów do określonego hosta oraz mierzenie opóźnień na każdym etapie tej trasy.

## Użycie
Podstawowa składnia polecenia `mtr` jest następująca:

```csh
mtr [opcje] [argumenty]
```

## Częste opcje
- `-r` : Uruchamia `mtr` w trybie raportu, wyświetlając wyniki w formacie tekstowym.
- `-c <liczba>` : Określa liczbę wysyłanych pakietów (domyślnie 10).
- `-n` : Nie rozwiązuje nazw hostów, pokazując jedynie adresy IP.
- `-i <czas>` : Ustala czas oczekiwania między wysyłanymi pakietami (w sekundach).

## Przykłady
1. **Podstawowe użycie mtr**:
   ```csh
   mtr example.com
   ```

2. **Uruchomienie w trybie raportu**:
   ```csh
   mtr -r example.com
   ```

3. **Określenie liczby wysyłanych pakietów**:
   ```csh
   mtr -c 5 example.com
   ```

4. **Nie rozwiązywanie nazw hostów**:
   ```csh
   mtr -n example.com
   ```

5. **Ustalenie czasu oczekiwania między pakietami**:
   ```csh
   mtr -i 0.5 example.com
   ```

## Wskazówki
- Używaj opcji `-n`, gdy chcesz uzyskać szybkie wyniki bez opóźnienia spowodowanego rozwiązywaniem nazw.
- W trybie raportu (`-r`) możesz łatwo zapisać wyniki do pliku, co jest przydatne do późniejszej analizy.
- Regularne monitorowanie trasy do kluczowych serwerów może pomóc w identyfikacji problemów z łącznością w czasie rzeczywistym.