# [Linux] Bash col bruk: [fjerner kontrolltegn fra tekst]

## Oversikt
`col` er et Bash-kommando som brukes til å fjerne kontrolltegn fra tekst, vanligvis fra tekststrømmer som genereres av andre kommandoer. Dette kan være nyttig når man ønsker å formatere utdataene for bedre lesbarhet, spesielt når man arbeider med tekst som inneholder formateringskontroller.

## Bruk
Grunnleggende syntaks for `col`-kommandoen er som følger:

```bash
col [alternativer] [argumenter]
```

## Vanlige alternativer
- `-b`: Fjerner backspaces og formateringskontroller fra teksten.
- `-x`: Behandler teksten som om den er i en "tabulator"-format, noe som kan være nyttig for å opprettholde kolonnejustering.
- `-f`: Konverterer formaterte tekst til en enkel tekst.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `col` kan brukes:

1. **Fjerne kontrolltegn fra en fil:**

   ```bash
   col -b < fil.txt > ny_fil.txt
   ```

   Dette fjerner backspaces fra `fil.txt` og lagrer resultatet i `ny_fil.txt`.

2. **Bruke col med en pipet strøm:**

   ```bash
   ls -l | col -b
   ```

   Her brukes `col` til å fjerne kontrolltegn fra utdataene av `ls -l`-kommandoen.

3. **Behandle tekst med tabulatorer:**

   ```bash
   cat fil.txt | col -x
   ```

   Dette vil konvertere tabulatorer i `fil.txt` til passende mellomrom for bedre lesbarhet.

## Tips
- Bruk `col -b` når du jobber med tekst som kan inneholde formateringskontroller for å sikre at utdataene er rene og lettleste.
- Kombiner `col` med andre kommandoer ved hjelp av pipe (`|`) for å effektivt håndtere tekststrømmer.
- Test alltid utdataene etter å ha brukt `col` for å sikre at formatet er som forventet.