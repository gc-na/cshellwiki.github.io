# [Bash] Bash head utilizare: [afiseaza primele linii ale unui fisier]

## Overview
Comanda `head` este utilizată în Bash pentru a afișa primele linii ale unui fișier. Este utilă pentru a obține o previzualizare rapidă a conținutului unui fișier mare fără a-l deschide complet.

## Usage
Sintaxa de bază a comenzii `head` este următoarea:

```bash
head [opțiuni] [argumente]
```

## Common Options
- `-n [număr]`: Specifică numărul de linii de afișat (de default, 10).
- `-c [număr]`: Afișează un număr specificat de octeți din începutul fișierului.
- `-q`: Nu afișează numele fișierului înainte de conținutul său.
- `-v`: Afișează numele fișierului înainte de conținutul său, chiar dacă este un singur fișier.

## Common Examples
1. Afișarea primelor 10 linii dintr-un fișier:
   ```bash
   head nume_fisier.txt
   ```

2. Afișarea primelor 5 linii dintr-un fișier:
   ```bash
   head -n 5 nume_fisier.txt
   ```

3. Afișarea primelor 100 de octeți dintr-un fișier:
   ```bash
   head -c 100 nume_fisier.txt
   ```

4. Afișarea primelor 10 linii dintr-un fișier și a numelui acestuia:
   ```bash
   head -v nume_fisier.txt
   ```

5. Afișarea primelor 10 linii din mai multe fișiere:
   ```bash
   head fisier1.txt fisier2.txt
   ```

## Tips
- Folosește opțiunea `-n` pentru a ajusta numărul de linii afișate, în funcție de nevoile tale.
- Comanda `head` poate fi combinată cu alte comenzi prin pipe pentru a obține rezultate mai complexe.
- Este util să folosești `head` împreună cu comanda `tail` pentru a analiza porțiuni specifice ale fișierelor.