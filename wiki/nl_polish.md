# [Linux] Bash nl użycie: numerowanie linii w plikach tekstowych

## Overview
Polecenie `nl` służy do numerowania linii w plikach tekstowych. Umożliwia dodanie numerów do każdej linii, co jest przydatne w przypadku analizy lub edytowania plików tekstowych.

## Usage
Podstawowa składnia polecenia `nl` jest następująca:

```
nl [opcje] [argumenty]
```

## Common Options
- `-b` : Określa sposób numerowania linii (np. `-b a` dla numerowania wszystkich linii).
- `-f` : Określa, które linie mają być numerowane (np. `-f 2` dla numerowania od drugiej linii).
- `-n` : Określa format numeracji (np. `-n ln` dla numeracji z wiodącymi zerami).
- `-w` : Ustawia szerokość numeru (np. `-w 3` dla szerokości 3 znaków).

## Common Examples
1. Numerowanie wszystkich linii w pliku:
   ```bash
   nl plik.txt
   ```

2. Numerowanie linii, zaczynając od drugiej:
   ```bash
   nl -f 2 plik.txt
   ```

3. Ustawienie szerokości numeru na 4 znaki:
   ```bash
   nl -w 4 plik.txt
   ```

4. Numerowanie tylko niepustych linii:
   ```bash
   nl -b t plik.txt
   ```

## Tips
- Używaj opcji `-n` do dostosowania formatu numeracji, aby lepiej pasował do Twoich potrzeb.
- Możesz przekierować wynik do nowego pliku, używając `>`:
  ```bash
  nl plik.txt > numerowany_plik.txt
  ```
- Eksperymentuj z różnymi opcjami, aby zobaczyć, jak zmieniają one wynik numeracji.