# [Linux] C Shell (csh) historia użycia: przeglądanie historii poleceń

## Overview
Polecenie `history` w C Shell (csh) służy do wyświetlania listy wcześniej wprowadzonych poleceń. Umożliwia użytkownikom przeglądanie, powtarzanie i zarządzanie historią poleceń, co może znacznie przyspieszyć pracę w terminalu.

## Usage
Podstawowa składnia polecenia `history` jest następująca:

```csh
history [options] [arguments]
```

## Common Options
- `-c` - Czyści historię poleceń.
- `-n` - Ładuje historię poleceń z pliku, ale nie zapisuje aktualnej historii.
- `-r` - Odczytuje historię poleceń z pliku.
- `-w` - Zapisuje aktualną historię poleceń do pliku.

## Common Examples
1. **Wyświetlenie historii poleceń:**
   ```csh
   history
   ```

2. **Czyszczenie historii poleceń:**
   ```csh
   history -c
   ```

3. **Zapisanie historii do pliku:**
   ```csh
   history -w
   ```

4. **Wczytanie historii z pliku:**
   ```csh
   history -r
   ```

5. **Wyświetlenie ostatnich 10 poleceń:**
   ```csh
   history 10
   ```

## Tips
- Regularnie przeglądaj historię, aby szybko odnaleźć wcześniej używane polecenia.
- Użyj opcji `-w`, aby zapisać historię przed zamknięciem sesji, co pozwoli na jej późniejsze wykorzystanie.
- Pamiętaj, że czyszczenie historii za pomocą `-c` jest nieodwracalne, więc używaj tej opcji ostrożnie.