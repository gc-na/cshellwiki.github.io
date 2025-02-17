# [Linux] Bash tee bruk: Kopier standardutgang til filer

## Oversikt
`tee`-kommandoen i Bash brukes til å lese standardutgang fra en kommando og skrive den til både standardutgang (skjermen) og en eller flere filer. Dette er nyttig når du ønsker å se utdataene samtidig som du lagrer dem for senere bruk.

## Bruk
Grunnleggende syntaks for `tee`-kommandoen er som følger:

```bash
tee [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`, `--append`: Legger til utdataene i slutten av filen i stedet for å overskrive den.
- `-i`, `--ignore-interrupts`: Ignorerer avbruddssignaler.
- `--help`: Viser hjelp og informasjon om bruken av `tee`.
- `--version`: Viser versjonsinformasjon om `tee`.

## Vanlige eksempler

1. **Skrive utdata til en fil og vise dem på skjermen:**
   ```bash
   echo "Hei, verden!" | tee fil.txt
   ```

2. **Legge til utdata i en eksisterende fil:**
   ```bash
   echo "Ny linje" | tee -a fil.txt
   ```

3. **Bruke `tee` med flere filer:**
   ```bash
   echo "Data til flere filer" | tee fil1.txt fil2.txt
   ```

4. **Kombinere `tee` med andre kommandoer:**
   ```bash
   ls -l | tee fil.txt | grep "txt"
   ```

## Tips
- Bruk `-a`-alternativet når du ønsker å bevare eksisterende innhold i filen.
- Kombiner `tee` med andre kommandoer for å filtrere eller manipulere utdataene før de lagres.
- Husk at `tee` kan brukes i skript for å logge utdataene fra kommandoer for feilsøking.