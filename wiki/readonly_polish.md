# [Linux] Bash readonly użycie: Ustawianie zmiennych jako tylko do odczytu

## Overview
Polecenie `readonly` w Bash służy do oznaczania zmiennych jako tylko do odczytu. Oznacza to, że po ustawieniu zmiennej jako readonly, nie można jej zmienić ani usunąć w bieżącej sesji skryptu. Jest to przydatne w sytuacjach, gdy chcemy zabezpieczyć ważne dane przed przypadkowymi modyfikacjami.

## Usage
Podstawowa składnia polecenia `readonly` jest następująca:

```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: Wyświetla wszystkie zmienne readonly w bieżącym środowisku.

## Common Examples

### Przykład 1: Ustawienie zmiennej jako readonly
```bash
my_var="Hello, World!"
readonly my_var
```
W tym przykładzie zmienna `my_var` jest ustawiana jako readonly, co oznacza, że nie można jej zmienić.

### Przykład 2: Próba zmiany zmiennej readonly
```bash
my_var="Hello, World!"
readonly my_var
my_var="New Value"  # To spowoduje błąd
```
Próba przypisania nowej wartości do `my_var` zakończy się błędem, ponieważ jest to zmienna readonly.

### Przykład 3: Wyświetlenie wszystkich zmiennych readonly
```bash
readonly -p
```
To polecenie wyświetli wszystkie zmienne, które zostały oznaczone jako readonly w bieżącej sesji.

## Tips
- Używaj `readonly` dla zmiennych, które powinny pozostać niezmienne w trakcie działania skryptu, aby uniknąć przypadkowych błędów.
- Pamiętaj, że zmienne readonly można nadal odczytywać, ale nie można ich modyfikować.
- Rozważ użycie `readonly` w skryptach, które są używane przez wiele osób, aby zapewnić integralność danych.