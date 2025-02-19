# [Linux] C Shell (csh) script Użycie: rejestrowanie sesji terminala

## Overview
Polecenie `script` w C Shell (csh) służy do rejestrowania sesji terminala. Umożliwia ono zapisanie wszystkich poleceń oraz ich wyników do pliku, co jest przydatne do późniejszego przeglądania lub dokumentacji.

## Usage
Podstawowa składnia polecenia `script` jest następująca:

```csh
script [opcje] [argumenty]
```

## Common Options
- `-a`: Dodaje dane do istniejącego pliku zamiast go nadpisywać.
- `-f`: Natychmiastowo zapisuje dane do pliku, co może być przydatne w przypadku długich sesji.
- `-q`: Wyłącza komunikaty informacyjne, co sprawia, że rejestracja jest bardziej dyskretna.

## Common Examples
1. Rozpoczęcie rejestrowania sesji do pliku `sesja.txt`:
   ```csh
   script sesja.txt
   ```

2. Dodanie nowej sesji do istniejącego pliku `sesja.txt`:
   ```csh
   script -a sesja.txt
   ```

3. Rejestrowanie sesji z natychmiastowym zapisem:
   ```csh
   script -f sesja.txt
   ```

4. Rozpoczęcie rejestrowania sesji bez komunikatów:
   ```csh
   script -q sesja.txt
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do zapisu w katalogu, w którym chcesz utworzyć plik rejestru.
- Możesz zakończyć rejestrowanie sesji, wpisując polecenie `exit` lub naciskając `Ctrl+D`.
- Regularnie przeglądaj pliki rejestru, aby upewnić się, że zawierają wszystkie potrzebne informacje.