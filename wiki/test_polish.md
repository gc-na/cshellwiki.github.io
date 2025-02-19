# [Linux] C Shell (csh) test użycie: Sprawdzanie warunków

## Overview
Polecenie `test` w C Shell (csh) służy do oceny warunków logicznych. Umożliwia sprawdzenie różnych warunków, takich jak istnienie plików, porównania wartości czy sprawdzanie typów danych. Jest to przydatne narzędzie w skryptach powłoki do podejmowania decyzji na podstawie wyników testów.

## Usage
Podstawowa składnia polecenia `test` wygląda następująco:

```csh
test [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `test`:

- `-e [plik]` - Sprawdza, czy plik istnieje.
- `-f [plik]` - Sprawdza, czy podany argument jest plikiem regularnym.
- `-d [katalog]` - Sprawdza, czy podany argument jest katalogiem.
- `-z [ciąg]` - Sprawdza, czy długość ciągu jest równa zeru.
- `-n [ciąg]` - Sprawdza, czy długość ciągu jest większa od zera.
- `[wartość1] -eq [wartość2]` - Sprawdza, czy dwie wartości są równe.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `test`:

1. Sprawdzenie, czy plik istnieje:
   ```csh
   test -e myfile.txt && echo "Plik istnieje"
   ```

2. Sprawdzenie, czy argument jest katalogiem:
   ```csh
   test -d /home/user && echo "To jest katalog"
   ```

3. Porównanie dwóch liczb:
   ```csh
   a=5
   b=10
   test $a -eq $b && echo "Liczby są równe" || echo "Liczby są różne"
   ```

4. Sprawdzenie, czy ciąg jest pusty:
   ```csh
   str=""
   test -z "$str" && echo "Ciąg jest pusty"
   ```

## Tips
- Używaj operatorów logicznych (np. `&&`, `||`) do łączenia wielu warunków w jednym poleceniu.
- Pamiętaj, aby zawsze używać cudzysłowów wokół zmiennych, aby uniknąć błędów związanych z pustymi wartościami.
- Możesz używać polecenia `test` w połączeniu z instrukcjami warunkowymi, aby tworzyć bardziej złożone skrypty.