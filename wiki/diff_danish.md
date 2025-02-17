# [Linux] Bash diff brug: Sammenlign filer og mapper

## Overview
`diff` er et Bash-kommando, der bruges til at sammenligne indholdet af to filer eller mapper. Den viser forskellene mellem dem, hvilket gør det lettere at identificere ændringer og variationer.

## Usage
Den grundlæggende syntaks for `diff`-kommandoen er:

```bash
diff [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `diff`:

- `-u`: Vis forskelle i et "unified" format, som er lettere at læse.
- `-c`: Vis forskelle i et "context" format, der giver mere kontekst omkring ændringerne.
- `-i`: Ignorer forskelle i store og små bogstaver.
- `-w`: Ignorer forskelle i mellemrum.
- `-r`: Sammenlign mapper rekursivt.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du bruger `diff`:

1. Sammenlign to filer:
   ```bash
   diff fil1.txt fil2.txt
   ```

2. Sammenlign to filer med "unified" format:
   ```bash
   diff -u fil1.txt fil2.txt
   ```

3. Sammenlign to mapper rekursivt:
   ```bash
   diff -r mappe1/ mappe2/
   ```

4. Ignorer store og små bogstaver:
   ```bash
   diff -i fil1.txt fil2.txt
   ```

5. Vis forskelle med kontekst:
   ```bash
   diff -c fil1.txt fil2.txt
   ```

## Tips
- Brug `-u` for at få et mere læsbart output, især når du arbejder med koden.
- Hvis du sammenligner mapper, kan `-r` være meget nyttig for at se alle forskelle i underliggende filer.
- Overvej at gemme outputtet i en fil, hvis du skal analysere forskellene senere:
  ```bash
  diff -u fil1.txt fil2.txt > forskelle.txt
  ```