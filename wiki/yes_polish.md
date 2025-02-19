# [Linux] C Shell (csh) yes użycie: generowanie niekończących się powtórzeń tekstu

## Overview
Polecenie `yes` w C Shell (csh) służy do generowania niekończącego się strumienia powtarzających się tekstów. Domyślnie wypisuje słowo "yes", ale można dostarczyć własny tekst jako argument.

## Usage
Podstawowa składnia polecenia `yes` jest następująca:

```csh
yes [opcje] [argumenty]
```

## Common Options
- `-h`, `--help`: Wyświetla pomoc dotyczącą polecenia `yes`.
- `-V`, `--version`: Wyświetla wersję polecenia `yes`.

## Common Examples
1. **Domyślne użycie**:
   Wypisuje "yes" w nieskończoność.
   ```csh
   yes
   ```

2. **Wypisywanie własnego tekstu**:
   Wypisuje "hello" w nieskończoność.
   ```csh
   yes hello
   ```

3. **Ograniczenie liczby powtórzeń**:
   Można użyć `head`, aby ograniczyć liczbę linii do 5.
   ```csh
   yes | head -n 5
   ```

4. **Zapis do pliku**:
   Wypisuje "yes" do pliku `output.txt`.
   ```csh
   yes > output.txt
   ```

## Tips
- Używaj `yes` w połączeniu z innymi poleceniami, aby automatycznie odpowiadać na pytania w skryptach.
- Uważaj na użycie `yes` bez ograniczeń, ponieważ może zająć dużo zasobów systemowych.
- Możesz użyć `Ctrl+C`, aby przerwać działanie polecenia `yes`, gdy nie jest już potrzebne.