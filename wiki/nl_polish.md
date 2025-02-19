# [Linux] C Shell (csh) nl użycie: numerowanie linii w plikach tekstowych

## Overview
Polecenie `nl` w C Shell (csh) służy do numerowania linii w plikach tekstowych. Umożliwia dodanie numerów do linii, co jest przydatne w przypadku przeglądania lub edytowania plików.

## Usage
Podstawowa składnia polecenia `nl` jest następująca:

```
nl [opcje] [argumenty]
```

## Common Options
- `-b` : Określa sposób numerowania linii (np. `-b a` numeruje wszystkie linie).
- `-f` : Określa, które linie mają być pomijane przy numerowaniu.
- `-n` : Umożliwia wybór formatu numerów (np. `-n ln` dla numerów lewostronnych).
- `-w` : Ustala szerokość numerów (np. `-w 4` dla czterocyfrowych numerów).

## Common Examples
1. Numerowanie wszystkich linii w pliku:
   ```csh
   nl plik.txt
   ```

2. Numerowanie tylko niepustych linii:
   ```csh
   nl -b a plik.txt
   ```

3. Pomijanie pierwszych 2 linii przy numerowaniu:
   ```csh
   nl -f 2 plik.txt
   ```

4. Ustawienie szerokości numerów na 5:
   ```csh
   nl -w 5 plik.txt
   ```

5. Zapisanie wyników do nowego pliku:
   ```csh
   nl plik.txt > numerowany_plik.txt
   ```

## Tips
- Używaj opcji `-b` do dostosowania numeracji w zależności od potrzeb.
- Sprawdzaj różne formaty numerów z opcją `-n`, aby uzyskać pożądany wygląd.
- Łącz `nl` z innymi poleceniami, takimi jak `grep` lub `sort`, aby uzyskać bardziej złożone wyniki.