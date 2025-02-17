# [Linux] Bash time użycie: Mierzenie czasu wykonywania poleceń

## Overview
Polecenie `time` w Bashu służy do mierzenia czasu wykonywania innych poleceń. Umożliwia użytkownikom analizę wydajności skryptów i programów, dostarczając informacji o czasie rzeczywistym, czasie CPU oraz pamięci używanej podczas wykonywania polecenia.

## Usage
Podstawowa składnia polecenia `time` jest następująca:

```bash
time [options] [arguments]
```

## Common Options
- `-p`: Wyświetla czas w formacie POSIX.
- `-o FILE`: Zapisuje wyniki do pliku zamiast wyświetlać je na standardowym wyjściu.
- `-v`: Wyświetla szczegółowe informacje o użyciu zasobów.

## Common Examples
1. Mierzenie czasu wykonywania prostego polecenia:
   ```bash
   time ls -l
   ```

2. Zapisanie wyników do pliku:
   ```bash
   time -o wynik.txt sleep 2
   ```

3. Użycie opcji szczegółowych:
   ```bash
   time -v find / -name "*.txt"
   ```

4. Mierzenie czasu skryptu:
   ```bash
   time bash my_script.sh
   ```

## Tips
- Używaj opcji `-v`, aby uzyskać bardziej szczegółowe informacje o użyciu pamięci i CPU.
- Zapisuj wyniki do pliku, aby móc je później analizować.
- Testuj różne polecenia, aby zrozumieć, które z nich są najbardziej czasochłonne i wymagają optymalizacji.