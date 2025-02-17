# [Linux] Bash export użycie: Ustawianie zmiennych środowiskowych

## Overview
Polecenie `export` w Bash służy do ustawiania zmiennych środowiskowych, które są dostępne dla wszystkich procesów uruchamianych w danej sesji powłoki. Dzięki temu możesz przekazywać informacje do programów i skryptów, które uruchamiasz.

## Usage
Podstawowa składnia polecenia `export` jest następująca:

```bash
export [opcje] [argumenty]
```

## Common Options
- `-n`: Usuwa zmienną z listy eksportowanych zmiennych.
- `-p`: Wyświetla wszystkie zmienne środowiskowe, które są aktualnie eksportowane.

## Common Examples
1. **Ustawienie zmiennej środowiskowej:**
   ```bash
   export MY_VAR="Hello, World!"
   ```

2. **Sprawdzenie wartości zmiennej:**
   ```bash
   echo $MY_VAR
   ```

3. **Eksportowanie zmiennej i uruchamianie programu:**
   ```bash
   export PATH=$PATH:/usr/local/bin
   ```

4. **Usunięcie zmiennej z eksportu:**
   ```bash
   export -n MY_VAR
   ```

5. **Wyświetlenie wszystkich eksportowanych zmiennych:**
   ```bash
   export -p
   ```

## Tips
- Zmienne eksportowane w jednej sesji powłoki nie są dostępne w innych sesjach. Aby były dostępne po ponownym uruchomieniu powłoki, dodaj je do pliku konfiguracyjnego, takiego jak `.bashrc`.
- Używaj nazw zmiennych, które są łatwe do zrozumienia, aby ułatwić sobie późniejsze zarządzanie nimi.
- Pamiętaj, że zmienne środowiskowe są czułe na wielkość liter, więc `MY_VAR` i `my_var` będą traktowane jako różne zmienne.