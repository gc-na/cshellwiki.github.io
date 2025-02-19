# [Linux] C Shell (csh) grep utilizare: Căutarea textului în fișiere

## Overview
Comanda `grep` este utilizată pentru a căuta un text specific în fișiere. Aceasta returnează liniile care conțin șirul de caractere căutat, fiind un instrument esențial pentru analiza și manipularea textului în sistemele de operare Unix și Linux.

## Usage
Sintaxa de bază a comenzii `grep` este următoarea:

```
grep [opțiuni] [argumente]
```

## Common Options
- `-i`: Ignoră diferențele între litere mari și mici.
- `-v`: Afișează liniile care nu conțin șirul căutat.
- `-r`: Caută recursiv în directoare.
- `-n`: Afișează numerele liniilor în care apare șirul căutat.
- `-l`: Afișează doar numele fișierelor care conțin șirul căutat.

## Common Examples
1. Căutarea unui șir de caractere într-un fișier:
   ```csh
   grep "text_cautat" fisier.txt
   ```

2. Căutarea unui șir de caractere fără a ține cont de litere:
   ```csh
   grep -i "text_cautat" fisier.txt
   ```

3. Căutarea recursivă într-un director:
   ```csh
   grep -r "text_cautat" /cale/catre/director
   ```

4. Afișarea liniilor care nu conțin șirul căutat:
   ```csh
   grep -v "text_cautat" fisier.txt
   ```

5. Afișarea numerelor liniilor în care apare șirul:
   ```csh
   grep -n "text_cautat" fisier.txt
   ```

## Tips
- Folosește opțiunea `-i` pentru a evita problemele cu literele mari și mici, mai ales când nu ești sigur de formatul textului.
- Combină `grep` cu alte comenzi folosind pipe (`|`) pentru a filtra rezultatele. De exemplu:
  ```csh
  cat fisier.txt | grep "text_cautat"
  ```
- Salvează rezultatele căutării într-un fișier folosind redirecționarea:
  ```csh
  grep "text_cautat" fisier.txt > rezultate.txt
  ```