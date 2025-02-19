# [Linux] C Shell (csh) strace użycie: Śledzenie wywołań systemowych

## Overview
Polecenie `strace` służy do śledzenia wywołań systemowych i sygnałów, które są generowane przez procesy w systemie operacyjnym. Umożliwia to programistom i administratorom systemów analizowanie interakcji aplikacji z jądrem systemu, co jest przydatne w debugowaniu i optymalizacji.

## Usage
Podstawowa składnia polecenia `strace` wygląda następująco:

```csh
strace [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `strace`:

- `-c` - Podsumowuje statystyki wywołań systemowych.
- `-f` - Śledzi również procesy potomne.
- `-o <plik>` - Zapisuje wyniki do określonego pliku.
- `-p <pid>` - Śledzi już działający proces o podanym identyfikatorze PID.
- `-e <wyrażenie>` - Filtruje wywołania systemowe według określonego wyrażenia.

## Common Examples
Oto kilka praktycznych przykładów użycia `strace`:

1. Śledzenie nowego procesu:
   ```csh
   strace ls
   ```

2. Śledzenie procesu z zapisem wyników do pliku:
   ```csh
   strace -o wynik.txt ls
   ```

3. Śledzenie procesu potomnego:
   ```csh
   strace -f ls
   ```

4. Śledzenie już działającego procesu:
   ```csh
   strace -p 1234
   ```

5. Podsumowanie wywołań systemowych:
   ```csh
   strace -c ls
   ```

## Tips
- Używaj opcji `-o`, aby zapisać wyniki do pliku, co ułatwia analizę.
- Filtruj wywołania za pomocą opcji `-e`, aby skupić się na interesujących cię systemowych wywołaniach.
- Pamiętaj, że `strace` może spowolnić działanie programu, dlatego najlepiej używać go w środowisku testowym.