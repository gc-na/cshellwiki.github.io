# [Linux] C Shell (csh) sort utilizare: Sortează liniile din fișiere text

## Overview
Comanda `sort` este utilizată pentru a organiza liniile din fișiere text într-o ordine specificată, fie că este vorba de ordine alfabetică, numerică sau inversă. Aceasta este o unealtă esențială pentru manipularea datelor în linie de comandă.

## Usage
Sintaxa de bază a comenzii `sort` este următoarea:

```csh
sort [options] [arguments]
```

## Common Options
- `-r`: Sortează în ordine inversă.
- `-n`: Sortează numeric, în loc de alfabetic.
- `-k`: Specifică cheia de sortare (coloana).
- `-u`: Elimină duplicatele din rezultatul sortat.
- `-o`: Scrie rezultatul sortării într-un fișier specificat.

## Common Examples
1. Sortează un fișier text în ordine alfabetică:
   ```csh
   sort fisier.txt
   ```

2. Sortează un fișier text în ordine inversă:
   ```csh
   sort -r fisier.txt
   ```

3. Sortează un fișier text numeric:
   ```csh
   sort -n fisier_numeric.txt
   ```

4. Sortează un fișier text pe baza unei coloane specifice (de exemplu, a doua coloană):
   ```csh
   sort -k 2 fisier.txt
   ```

5. Elimină duplicatele dintr-un fișier sortat:
   ```csh
   sort -u fisier.txt
   ```

6. Scrie rezultatul sortării într-un alt fișier:
   ```csh
   sort fisier.txt -o fisier_sortat.txt
   ```

## Tips
- Folosește opțiunea `-n` pentru a evita sortarea greșită a numerelor (de exemplu, "10" înainte de "2").
- Combină opțiunile pentru a obține rezultatele dorite, cum ar fi `sort -r -n` pentru a sorta numeric în ordine inversă.
- Verifică întotdeauna rezultatul sortării, mai ales când lucrezi cu fișiere mari sau importante.