# [Linux] C Shell (csh) nslookup użycie: Sprawdzanie informacji o DNS

## Overview
Polecenie `nslookup` służy do uzyskiwania informacji o systemie nazw domen (DNS). Umożliwia użytkownikom wyszukiwanie adresów IP dla nazw domen oraz odwrotnie, co jest przydatne w diagnostyce problemów z siecią.

## Usage
Podstawowa składnia polecenia `nslookup` wygląda następująco:

```csh
nslookup [opcje] [argumenty]
```

## Common Options
- `-type=typ`: Określa typ rekordu DNS do wyszukania (np. A, MX, CNAME).
- `-timeout=n`: Ustala czas oczekiwania na odpowiedź w sekundach.
- `-retry=n`: Ustala liczbę prób ponownego wysłania zapytania.
- `-debug`: Włącza tryb debugowania, co pozwala na uzyskanie bardziej szczegółowych informacji o zapytaniach.

## Common Examples
Przykłady użycia polecenia `nslookup`:

1. Wyszukiwanie adresu IP dla domeny:
   ```csh
   nslookup example.com
   ```

2. Wyszukiwanie rekordu MX dla domeny:
   ```csh
   nslookup -type=MX example.com
   ```

3. Ustalanie serwera DNS do użycia:
   ```csh
   nslookup example.com 8.8.8.8
   ```

4. Włączenie trybu debugowania:
   ```csh
   nslookup -debug example.com
   ```

## Tips
- Używaj opcji `-type` do precyzyjnego określenia rodzaju rekordu, którego szukasz, aby uzyskać bardziej trafne wyniki.
- Sprawdzaj różne serwery DNS, aby zweryfikować, czy problem nie leży po stronie konkretnego serwera.
- Regularnie korzystaj z opcji `-debug`, aby zrozumieć, jak działają zapytania DNS i diagnozować problemy.