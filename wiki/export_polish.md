# [Linux] C Shell (csh) export użycie: Umożliwia ustawienie zmiennych środowiskowych

## Overview
Polecenie `export` w C Shell (csh) służy do ustawiania zmiennych środowiskowych, które są dostępne dla wszystkich procesów uruchomionych w danej sesji powłoki. Dzięki temu można przekazywać wartości zmiennych do programów i skryptów, które są uruchamiane w tej samej sesji.

## Usage
Podstawowa składnia polecenia `export` wygląda następująco:

```csh
export [opcje] [argumenty]
```

## Common Options
- `-n`: Usuwa zmienną z listy zmiennych eksportowanych.
- `-p`: Wyświetla wszystkie zmienne, które są aktualnie eksportowane.

## Common Examples
1. Ustawienie zmiennej środowiskowej:
   ```csh
   setenv MY_VAR "Hello, World!"
   export MY_VAR
   ```

2. Ustawienie zmiennej z wartością i jej eksport:
   ```csh
   setenv PATH "/usr/local/bin:$PATH"
   export PATH
   ```

3. Usunięcie zmiennej z eksportu:
   ```csh
   export -n MY_VAR
   ```

4. Wyświetlenie wszystkich eksportowanych zmiennych:
   ```csh
   export -p
   ```

## Tips
- Zawsze używaj `setenv` do tworzenia zmiennych przed ich eksportowaniem.
- Sprawdzaj, które zmienne są eksportowane, aby uniknąć konfliktów nazw.
- Pamiętaj, że zmienne eksportowane będą dostępne tylko w bieżącej sesji powłoki i jej podprocesach.