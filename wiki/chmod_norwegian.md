# [Linux] Bash chmod bruk: Endre filrettigheter

## Oversikt
`chmod` (change mode) er en Bash-kommando som brukes til å endre tilgangsrettighetene til filer og kataloger i Unix-lignende operativsystemer. Denne kommandoen lar brukere spesifisere hvilke rettigheter som skal gis eller fjernes for eier, gruppe og andre.

## Bruk
Grunnleggende syntaks for `chmod`-kommandoen er som følger:

```bash
chmod [alternativer] [rettigheter] [fil/katalog]
```

## Vanlige alternativer
- `-R`: Rekursiv endring av rettigheter for alle filer og underkataloger.
- `-v`: Vis detaljer om hva som endres.
- `-c`: Vis bare endringer som faktisk ble gjort.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `chmod` kan brukes:

1. **Gi eieren skrive- og leserettigheter:**
   ```bash
   chmod u+rw fil.txt
   ```

2. **Fjerne skrivetilgang for gruppen:**
   ```bash
   chmod g-w fil.txt
   ```

3. **Sett rettigheter til 755 for en katalog:**
   ```bash
   chmod 755 katalog/
   ```

4. **Rekursivt gi alle rettigheter til eieren:**
   ```bash
   chmod -R u+rwx katalog/
   ```

5. **Vis endringer som gjøres:**
   ```bash
   chmod -v 644 fil.txt
   ```

## Tips
- Bruk `chmod` med omhu, spesielt når du gir utvidede rettigheter som skrivetilgang.
- For å unngå utilsiktede endringer, kan det være lurt å bruke `-c` alternativet for å se hva som faktisk endres.
- Husk at rettighetene kan angis både med symboler (u, g, o) og numeriske verdier (0-7), så velg den metoden som passer best for ditt behov.