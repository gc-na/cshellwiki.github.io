# [Linux] C Shell (csh) cp Utilizare: Copierea fișierelor și directoarelor

## Overview
Comanda `cp` este utilizată pentru a copia fișiere și directoare în sistemul de operare. Aceasta permite utilizatorilor să creeze copii ale fișierelor existente sau să mute fișiere între diferite locații.

## Usage
Sintaxa de bază a comenzii `cp` este următoarea:

```csh
cp [opțiuni] [argumente]
```

## Common Options
- `-i`: Solicita confirmarea înainte de a suprascrie un fișier existent.
- `-r`: Copiază recursiv directoare și conținutul acestora.
- `-u`: Copiază fișierele doar dacă sursa este mai nouă decât destinația sau dacă destinația nu există.
- `-v`: Afișează informații detaliate despre fișierele copiate.

## Common Examples
1. **Copierea unui fișier:**
   ```csh
   cp fisier.txt copia_fisier.txt
   ```

2. **Copierea unui director și a conținutului său:**
   ```csh
   cp -r director_original director_copie
   ```

3. **Copierea unui fișier cu confirmare înainte de suprascriere:**
   ```csh
   cp -i fisier_vechi.txt fisier_nou.txt
   ```

4. **Copierea fișierelor doar dacă sursa este mai recentă:**
   ```csh
   cp -u fisier.txt director_destinatie/
   ```

5. **Afișarea detaliilor în timpul copiei:**
   ```csh
   cp -v fisier.txt director_destinatie/
   ```

## Tips
- Folosiți opțiunea `-i` pentru a evita suprascrierea accidentală a fișierelor importante.
- Când copiați directoare, nu uitați să folosiți opțiunea `-r` pentru a include toate subdirectoarele și fișierele.
- Verificați întotdeauna calea de destinație pentru a vă asigura că copiați fișierele în locația dorită.