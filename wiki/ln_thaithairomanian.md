# [Linux] Bash ln <Utilizare echivalentă în română>: [creați legături între fișiere]

## Overview
Comanda `ln` este utilizată în Bash pentru a crea legături între fișiere. Aceasta permite utilizatorilor să creeze legături simbolice sau hard link-uri, facilitând accesul la fișiere din locații diferite fără a le copia efectiv.

## Usage
Sintaxa de bază a comenzii `ln` este următoarea:

```bash
ln [opțiuni] [argumente]
```

## Common Options
- `-s`: Creează o legătură simbolică în loc de un hard link.
- `-f`: Forțează crearea legăturii, suprascriind fișierele existente.
- `-n`: Nu urmează legăturile simbolice existente.
- `-v`: Afișează informații detaliate despre acțiunile efectuate.

## Common Examples
1. **Crearea unui hard link:**
   ```bash
   ln /cale/catre/fișier.txt /cale/catre/legătură.txt
   ```

2. **Crearea unei legături simbolice:**
   ```bash
   ln -s /cale/catre/fișier.txt /cale/catre/legătură_simbolică.txt
   ```

3. **Forțarea creării unei legături:**
   ```bash
   ln -f /cale/catre/fișier.txt /cale/catre/legătură.txt
   ```

4. **Crearea unei legături simbolice cu detalii:**
   ```bash
   ln -sv /cale/catre/fișier.txt /cale/catre/legătură_simbolică.txt
   ```

## Tips
- Utilizați legăturile simbolice pentru a economisi spațiu pe disc, mai ales când lucrați cu fișiere mari.
- Verificați întotdeauna calea fișierului sursă pentru a evita erorile de legătură.
- Folosiți opțiunea `-v` pentru a obține feedback vizual despre acțiunile efectuate, mai ales când lucrați cu mai multe fișiere.