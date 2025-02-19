# [Linux] C Shell (csh) basename utilizare: Extrage numele fișierului dintr-o cale

## Overview
Comanda `basename` este utilizată pentru a extrage numele fișierului dintr-o cale completă. Aceasta elimină toate componentele de director dintr-un nume de fișier, lăsând doar numele fișierului.

## Usage
Sintaxa de bază a comenzii `basename` este următoarea:
```
basename [opțiuni] [argumente]
```

## Common Options
- `-a`: Acceptă mai multe argumente și returnează numele de bază pentru fiecare.
- `-s`: Specifică un sufix care va fi eliminat din numele fișierului.

## Common Examples
1. Extrage numele fișierului dintr-o cale completă:
   ```csh
   basename /usr/local/bin/script.sh
   ```
   Rezultatul va fi:
   ```
   script.sh
   ```

2. Elimină un sufix specific din numele fișierului:
   ```csh
   basename /usr/local/bin/script.sh .sh
   ```
   Rezultatul va fi:
   ```
   script
   ```

3. Folosind opțiunea `-a` pentru a extrage numele de bază din mai multe căi:
   ```csh
   basename -a /usr/local/bin/script.sh /usr/bin/another_script.py
   ```
   Rezultatul va fi:
   ```
   script.sh
   another_script.py
   ```

## Tips
- Folosește `basename` în scripturi pentru a obține numele fișierelor fără a include căile complete, ceea ce poate facilita manipularea fișierelor.
- Combină `basename` cu alte comenzi, cum ar fi `find`, pentru a procesa fișierele într-un mod mai eficient.