# [Linux] C Shell (csh) find utilizare: găsirea numelui fișierelor

## Overview
Comanda `find` este utilizată pentru a căuta fișiere și directoare într-o structură de directoare, pe baza unor criterii specificate, cum ar fi numele, tipul sau data modificării.

## Usage
Sintaxa de bază a comenzii `find` este următoarea:

```
find [opțiuni] [argumente]
```

## Common Options
- `-name`: caută fișiere după nume.
- `-type`: specifică tipul de fișier (de exemplu, `f` pentru fișiere obișnuite, `d` pentru directoare).
- `-mtime`: caută fișiere modificate în ultimele N zile.
- `-size`: caută fișiere de o anumită dimensiune.
- `-exec`: execută o comandă pe fișierele găsite.

## Common Examples
1. Căutarea unui fișier după nume:
   ```csh
   find /cale/catre/director -name "fisier.txt"
   ```

2. Căutarea tuturor directoarelor:
   ```csh
   find /cale/catre/director -type d
   ```

3. Căutarea fișierelor modificate în ultimele 7 zile:
   ```csh
   find /cale/catre/director -mtime -7
   ```

4. Căutarea fișierelor mai mari de 1MB:
   ```csh
   find /cale/catre/director -size +1M
   ```

5. Executarea unei comenzi pe fișierele găsite:
   ```csh
   find /cale/catre/director -name "*.log" -exec rm {} \;
   ```

## Tips
- Folosiți `-print` pentru a afișa rezultatele căutării, deși este implicit în majoritatea versiunilor.
- Fiți atenți la utilizarea caracterelor wildcard (`*`, `?`) în numele fișierelor pentru a evita rezultate neașteptate.
- Testați comenzile cu opțiunea `-print` înainte de a folosi `-exec` pentru a verifica ce fișiere vor fi afectate.