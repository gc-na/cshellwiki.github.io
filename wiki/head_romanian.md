# [Linux] C Shell (csh) head utilizare: Afișează primele linii ale unui fișier

## Overview
Comanda `head` este utilizată pentru a afișa primele linii ale unui fișier. Este utilă pentru a obține rapid o previzualizare a conținutului unui fișier mare fără a-l deschide complet.

## Usage
Sintaxa de bază a comenzii `head` este următoarea:

```
head [options] [arguments]
```

## Common Options
- `-n [număr]`: Afișează primele `număr` de linii din fișier. Implicit, `head` afișează primele 10 linii.
- `-c [număr]`: Afișează primele `număr` de octeți din fișier.
- `-q`: Nu afișează numele fișierului înainte de conținutul acestuia, când se lucrează cu mai multe fișiere.
- `-v`: Afișează numele fișierului înainte de conținutul acestuia, chiar și atunci când se lucrează cu un singur fișier.

## Common Examples
1. Afișarea primelor 10 linii dintr-un fișier:
   ```csh
   head nume_fisier.txt
   ```

2. Afișarea primelor 5 linii dintr-un fișier:
   ```csh
   head -n 5 nume_fisier.txt
   ```

3. Afișarea primelor 100 de octeți dintr-un fișier:
   ```csh
   head -c 100 nume_fisier.txt
   ```

4. Afișarea primelor 10 linii din mai multe fișiere:
   ```csh
   head fisier1.txt fisier2.txt
   ```

5. Afișarea numelui fișierului și a conținutului său:
   ```csh
   head -v nume_fisier.txt
   ```

## Tips
- Folosește opțiunea `-n` pentru a personaliza numărul de linii afișate, în funcție de nevoile tale.
- Comanda `head` este adesea utilizată împreună cu alte comenzi, cum ar fi `grep`, pentru a filtra rezultatele.
- Dacă vrei să vezi ultimele linii ale unui fișier, poți folosi comanda `tail`, care funcționează similar cu `head`.