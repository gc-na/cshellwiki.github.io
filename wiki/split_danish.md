# [Linux] Bash split brug: Opdel filer i mindre stykker

## Oversigt
`split`-kommandoen bruges til at opdele en stor fil i mindre filer. Dette kan være nyttigt, når du arbejder med store datasæt eller ønsker at dele en fil for lettere håndtering.

## Brug
Den grundlæggende syntaks for `split`-kommandoen er:

```bash
split [muligheder] [argumenter]
```

## Almindelige muligheder
- `-b, --bytes=SIZE`: Angiv størrelsen på de opdelte filer i bytes.
- `-l, --lines=NUMBER`: Angiv antallet af linjer i hver opdelte fil.
- `-d, --numeric-suffixes`: Brug numeriske suffikser i stedet for alfabetiske.
- `--additional-suffix=SUFFIX`: Tilføj et ekstra suffiks til de opdelte filer.

## Almindelige eksempler

1. **Opdel en fil i stykker af 100 linjer:**
   ```bash
   split -l 100 storfil.txt
   ```

2. **Opdel en fil i stykker af 1 MB:**
   ```bash
   split -b 1M storfil.txt
   ```

3. **Brug numeriske suffikser:**
   ```bash
   split -d -l 50 storfil.txt
   ```

4. **Tilføj et ekstra suffiks til de opdelte filer:**
   ```bash
   split --additional-suffix=.txt -l 10 storfil.txt del_
   ```

## Tips
- Vær opmærksom på, at de opdelte filer vil få standardnavne som `xaa`, `xab`, osv. Du kan ændre dette ved at angive et præfiks.
- Brug `cat`-kommandoen til at samle de opdelte filer igen, hvis det er nødvendigt.
- Overvej at bruge `-d`-muligheden, hvis du arbejder med mange opdelte filer for at undgå forvirring med suffikserne.