# [Linux] C Shell (csh) comm: compararea fișierelor

## Overview
Comanda `comm` este utilizată pentru a compara două fișiere sortate linie cu linie. Aceasta afișează liniile care sunt unice pentru fiecare fișier, precum și liniile comune.

## Usage
Sintaxa de bază a comenzii este următoarea:

```
comm [opțiuni] [argumente]
```

## Common Options
- `-1`: Suprimă liniile unice din primul fișier.
- `-2`: Suprimă liniile unice din al doilea fișier.
- `-3`: Suprimă liniile comune.
- `-i`: Ignoră diferențele dintre literele mari și mici.

## Common Examples
1. Compararea a două fișiere și afișarea tuturor liniilor:
   ```csh
   comm file1.txt file2.txt
   ```

2. Afișarea doar a liniilor comune dintre două fișiere:
   ```csh
   comm -12 file1.txt file2.txt
   ```

3. Afișarea liniilor unice din primul fișier:
   ```csh
   comm -13 file1.txt file2.txt
   ```

4. Afișarea liniilor unice din al doilea fișier:
   ```csh
   comm -23 file1.txt file2.txt
   ```

5. Compararea fișierelor fără a ține cont de literele mari și mici:
   ```csh
   comm -i file1.txt file2.txt
   ```

## Tips
- Asigură-te că fișierele pe care le compari sunt sortate, altfel rezultatele nu vor fi corecte.
- Poți redirecționa ieșirea comenzii către un alt fișier pentru a salva rezultatele:
  ```csh
  comm file1.txt file2.txt > rezultate.txt
  ```
- Folosește opțiunile corespunzătoare pentru a obține exact informațiile de care ai nevoie, fără a fi copleșit de date inutile.