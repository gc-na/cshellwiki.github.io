# [Linux] Bash od bruksanvisning: vise filinnhold i forskjellige formater

## Oversikt
`od` (octal dump) er en kommando i Unix-lignende operativsystemer som brukes til å vise innholdet i filer i forskjellige formater, inkludert oktal, heksadesimal og ASCII. Den er nyttig for å inspisere binære filer eller for å analysere data på lavt nivå.

## Bruk
Grunnleggende syntaks for `od`-kommandoen er som følger:

```bash
od [alternativer] [argumenter]
```

## Vanlige alternativer
- `-A, --address-radix=RADIX`: Angir adressens radikse format (o for oktal, x for heksadesimal, d for desimal).
- `-t, --format=TYPE`: Angir formatet for utdata (f.eks. `c` for ASCII-tegn, `x` for heksadesimal).
- `-N, --bytes=NUM`: Angir antall bytes som skal vises.
- `-v, --output-duplicates`: Viser alle data, inkludert duplikater.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `od`-kommandoen:

1. Vise innholdet i en fil i heksadesimal format:
   ```bash
   od -x filnavn.txt
   ```

2. Vise innholdet i en fil i oktal format:
   ```bash
   od -c filnavn.bin
   ```

3. Vise de første 16 byte av en fil i heksadesimal format:
   ```bash
   od -N 16 -t x filnavn.bin
   ```

4. Vise innholdet i en fil med adresse i desimal format:
   ```bash
   od -A d -t c filnavn.txt
   ```

## Tips
- Bruk `-v` alternativet hvis du vil se alle dataene, selv om de er duplikater.
- Kombiner `od` med `head` eller `tail` for å vise bare en del av filen:
  ```bash
  head -n 10 filnavn.txt | od
  ```
- Eksperimenter med forskjellige formater for å få en bedre forståelse av hvordan dataene er strukturert.