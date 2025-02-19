# [Linux] C Shell (csh) mkdir utilizare: Crearea de directoare

## Overview
Comanda `mkdir` este utilizată pentru a crea directoare noi în sistemul de fișiere. Aceasta permite utilizatorilor să organizeze fișierele și subdirectoarele într-o structură ierarhică.

## Usage
Sintaxa de bază a comenzii `mkdir` este următoarea:

```csh
mkdir [opțiuni] [argumente]
```

## Common Options
- `-p`: Creează directoare părinte, dacă acestea nu există deja.
- `-m`: Setează permisiunile pentru noul director, specificând un mod numeric.
- `-v`: Afișează un mesaj pentru fiecare director creat.

## Common Examples
1. Crearea unui singur director:
   ```csh
   mkdir nou_director
   ```

2. Crearea mai multor directoare simultan:
   ```csh
   mkdir director1 director2 director3
   ```

3. Crearea unui director părinte și a subdirectoarelor:
   ```csh
   mkdir -p parinte/subdirector1/subdirector2
   ```

4. Crearea unui director cu permisiuni specifice:
   ```csh
   mkdir -m 755 director_permisiuni
   ```

5. Afișarea mesajelor de confirmare pentru fiecare director creat:
   ```csh
   mkdir -v director_afisat
   ```

## Tips
- Folosiți opțiunea `-p` pentru a evita erorile atunci când creați o structură de directoare complexă.
- Verificați permisiunile după crearea unui director, mai ales dacă folosiți opțiunea `-m`.
- Utilizați `mkdir` în combinație cu alte comenzi, cum ar fi `cd`, pentru a naviga rapid în noile directoare create.