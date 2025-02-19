# [Linux] C Shell (csh) wc utilizare: Numără liniile, cuvintele și caracterele din fișiere

## Overview
Comanda `wc` (word count) este utilizată pentru a număra liniile, cuvintele și caracterele din fișierele text. Aceasta este o unealtă utilă pentru a obține rapid statistici despre conținutul fișierelor.

## Usage
Sintaxa de bază a comenzii `wc` este următoarea:
```csh
wc [options] [arguments]
```

## Common Options
- `-l`: Numără doar liniile din fișier.
- `-w`: Numără doar cuvintele din fișier.
- `-c`: Numără doar caracterele din fișier.
- `-m`: Numără caracterele, dar ține cont de caracterele multibyte.
- `-L`: Afișează lungimea celei mai lungi linii.

## Common Examples
1. Numărarea liniilor, cuvintelor și caracterelor dintr-un fișier:
   ```csh
   wc fisier.txt
   ```

2. Numărarea doar a liniilor dintr-un fișier:
   ```csh
   wc -l fisier.txt
   ```

3. Numărarea doar a cuvintelor dintr-un fișier:
   ```csh
   wc -w fisier.txt
   ```

4. Numărarea doar a caracterelor dintr-un fișier:
   ```csh
   wc -c fisier.txt
   ```

5. Numărarea lungimii celei mai lungi linii dintr-un fișier:
   ```csh
   wc -L fisier.txt
   ```

## Tips
- Folosește opțiunea `-l` pentru a verifica rapid numărul de linii din scripturi sau fișiere de log.
- Combină `wc` cu alte comenzi prin utilizarea pipe-ului (`|`) pentru a analiza ieșirea altor comenzi.
- Verifică documentația completă a comenzii `wc` folosind `man wc` pentru a descoperi opțiuni suplimentare.