# [Linux] C Shell (csh) mv utilizare: Mută sau redenumește fișiere

## Overview
Comanda `mv` este utilizată în C Shell (csh) pentru a muta sau redenumi fișiere și directoare. Aceasta permite utilizatorilor să organizeze și să gestioneze fișierele într-un mod eficient.

## Usage
Sintaxa de bază a comenzii `mv` este următoarea:

```csh
mv [opțiuni] [argumente]
```

## Common Options
- `-i`: Întreabă utilizatorul înainte de a suprascrie un fișier existent.
- `-f`: Forțează mutarea fișierului, fără a întreba utilizatorul, chiar dacă fișierul destinație există.
- `-u`: Mută fișierul doar dacă sursa este mai nouă decât destinația sau dacă destinația nu există.

## Common Examples
1. **Mutarea unui fișier într-un alt director:**
   ```csh
   mv document.txt /home/utilizator/documents/
   ```

2. **Redenumirea unui fișier:**
   ```csh
   mv vechi.txt nou.txt
   ```

3. **Mutarea mai multor fișiere într-un director:**
   ```csh
   mv *.jpg /home/utilizator/pictures/
   ```

4. **Mutarea unui fișier cu confirmare înainte de suprascriere:**
   ```csh
   mv -i document.txt /home/utilizator/documents/
   ```

## Tips
- Folosește opțiunea `-i` pentru a evita suprascrierea accidentală a fișierelor.
- Verifică întotdeauna calea destinație pentru a te asigura că fișierele sunt mutate în locul dorit.
- Poți folosi wildcard-uri (de exemplu, `*`) pentru a muta sau redenumi mai multe fișiere simultan.