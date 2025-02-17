# [Linux] Bash getopts użycie: Obsługa opcji w skryptach

## Overview
Polecenie `getopts` w Bashu służy do przetwarzania opcji w skryptach powłoki. Umożliwia łatwe zarządzanie argumentami przekazywanymi do skryptu, co pozwala na tworzenie bardziej interaktywnych i elastycznych programów.

## Usage
Podstawowa składnia polecenia `getopts` jest następująca:

```bash
getopts [options] [arguments]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `getopts`:

- `-a`: Umożliwia przetwarzanie opcji w formacie krótkim.
- `-b`: Umożliwia przetwarzanie opcji w formacie długim.
- `-c`: Umożliwia zdefiniowanie domyślnych wartości dla opcji.

## Common Examples

### Przykład 1: Prosty skrypt z jedną opcją
```bash
#!/bin/bash

while getopts "f:" opt; do
  case $opt in
    f) echo "Plik: $OPTARG" ;;
    *) echo "Nieznana opcja" ;;
  esac
done
```
W tym przykładzie skrypt przyjmuje jedną opcję `-f`, która oczekuje argumentu (nazwa pliku).

### Przykład 2: Skrypt z wieloma opcjami
```bash
#!/bin/bash

while getopts "a:b:c:" opt; do
  case $opt in
    a) echo "Opcja A: $OPTARG" ;;
    b) echo "Opcja B: $OPTARG" ;;
    c) echo "Opcja C: $OPTARG" ;;
    *) echo "Nieznana opcja" ;;
  esac
done
```
Ten skrypt obsługuje trzy opcje: `-a`, `-b` i `-c`, każda z własnym argumentem.

### Przykład 3: Użycie domyślnych wartości
```bash
#!/bin/bash

while getopts "a:b:c:" opt; do
  case $opt in
    a) opt_a=$OPTARG ;;
    b) opt_b=$OPTARG ;;
    c) opt_c=$OPTARG ;;
    *) echo "Nieznana opcja" ;;
  esac
done

# Ustawienie domyślnych wartości
opt_a=${opt_a:-"domyślna_a"}
opt_b=${opt_b:-"domyślna_b"}
opt_c=${opt_c:-"domyślna_c"}

echo "Opcja A: $opt_a"
echo "Opcja B: $opt_b"
echo "Opcja C: $opt_c"
```
W tym przykładzie skrypt ustawia domyślne wartości dla opcji, jeśli nie zostały one podane.

## Tips
- Zawsze używaj `getopts` w pętli `while`, aby przetwarzać wszystkie opcje przekazane do skryptu.
- Używaj `:` po literze opcji, aby wskazać, że opcja wymaga argumentu.
- Używaj zmiennej `$OPTARG`, aby uzyskać wartość argumentu dla danej opcji.
- Zawsze obsługuj nieznane opcje, aby użytkownik był informowany o błędach.