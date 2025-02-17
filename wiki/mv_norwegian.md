# [Linux] Bash mv Bruk: Flytt eller gi nytt navn til filer og mapper

## Oversikt
`mv`-kommandoen brukes til å flytte eller gi nytt navn til filer og mapper i Unix-lignende operativsystemer. Den kan også brukes til å omorganisere filstrukturen ved å flytte filer mellom forskjellige kataloger.

## Bruk
Grunnleggende syntaks for `mv`-kommandoen er som følger:

```bash
mv [alternativer] [kilde] [mål]
```

## Vanlige alternativer
- `-i`: Spør om bekreftelse før overskriving av eksisterende filer.
- `-u`: Flytt bare hvis kilden er nyere enn målet eller hvis målet ikke finnes.
- `-v`: Vis detaljer om hva som skjer under flyttingen.
- `-n`: Ikke overskriv eksisterende filer.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `mv`-kommandoen kan brukes:

1. **Flytte en fil til en annen katalog:**
   ```bash
   mv fil.txt /sti/til/mål/
   ```

2. **Gi nytt navn til en fil:**
   ```bash
   mv gammel_fil.txt ny_fil.txt
   ```

3. **Flytte flere filer til en katalog:**
   ```bash
   mv fil1.txt fil2.txt /sti/til/mål/
   ```

4. **Bruke alternativet -i for å unngå overskriving:**
   ```bash
   mv -i fil.txt /sti/til/mål/
   ```

5. **Flytte en katalog:**
   ```bash
   mv /sti/til/kilde_katalog /sti/til/mål_katalog
   ```

## Tips
- Bruk `-v` alternativet for å se hva som skjer når du flytter filer, spesielt når du jobber med mange filer.
- Vær forsiktig med `mv`-kommandoen, da den kan overskrive eksisterende filer uten advarsel hvis ikke `-i` brukes.
- Når du gir nytt navn til filer, sørg for at det nye navnet ikke allerede er i bruk for å unngå tap av data.