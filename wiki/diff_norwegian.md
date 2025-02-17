# [Linux] Bash diff bruk: Sammenligne filer og vise forskjeller

## Oversikt
`diff`-kommandoen brukes til å sammenligne innholdet i to filer linje for linje. Den viser hvilke linjer som er forskjellige mellom de to filene, noe som er nyttig for å se endringer i tekstfiler, kildekode eller konfigurasjonsfiler.

## Bruk
Grunnleggende syntaks for `diff`-kommandoen er som følger:

```bash
diff [alternativer] [fil1] [fil2]
```

## Vanlige alternativer
- `-u`: Viser forskjeller i "unified" format, som er enklere å lese.
- `-c`: Viser forskjeller i "context" format, som gir mer kontekst rundt endringene.
- `-i`: Ignorerer forskjeller i store og små bokstaver.
- `-w`: Ignorerer forskjeller i hvite mellomrom.
- `-r`: Sammenligner kataloger rekursivt.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `diff`:

1. Sammenligne to tekstfiler:
   ```bash
   diff fil1.txt fil2.txt
   ```

2. Vise forskjeller i "unified" format:
   ```bash
   diff -u fil1.txt fil2.txt
   ```

3. Sammenligne to kataloger:
   ```bash
   diff -r katalog1/ katalog2/
   ```

4. Ignorere forskjeller i store og små bokstaver:
   ```bash
   diff -i fil1.txt fil2.txt
   ```

5. Vise forskjeller med kontekst:
   ```bash
   diff -c fil1.txt fil2.txt
   ```

## Tips
- Bruk `-u` alternativet for å få en mer lesbar utdata, spesielt når du jobber med kildekode.
- Når du sammenligner kataloger, kan `-r` være nyttig for å se alle forskjeller i underkataloger.
- Kombiner `diff` med `patch` for å bruke endringene fra en fil til en annen.