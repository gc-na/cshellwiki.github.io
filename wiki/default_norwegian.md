# [Linux] Bash standard kommando: [utfør kommandoer i bakgrunnen]

## Oversikt
Kommandoen `nohup` brukes til å kjøre en prosess i bakgrunnen, selv etter at brukeren har logget ut. Dette er nyttig for langvarige oppgaver som ikke skal stoppes når terminalvinduet lukkes.

## Bruk
Den grunnleggende syntaksen for `nohup` er som følger:

```bash
nohup [kommando] [argumenter] &
```

## Vanlige alternativer
- `&`: Kjører kommandoen i bakgrunnen.
- `nohup.out`: Standard utdatafil der utdata fra kommandoen blir lagret, med mindre en annen fil spesifiseres.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `nohup`:

1. Kjør en skriptfil i bakgrunnen:
   ```bash
   nohup ./mitt_skript.sh &
   ```

2. Kjør en langvarig prosess som `ping`:
   ```bash
   nohup ping google.com &
   ```

3. Lagre utdataene til en spesifikk fil:
   ```bash
   nohup ./langvarig_prosess.sh > utdata.txt &
   ```

## Tips
- Bruk `jobs`-kommandoen for å se bakgrunnsprosesser.
- Du kan bruke `fg` for å bringe en bakgrunnsprosess tilbake til forgrunnen.
- Husk å sjekke `nohup.out` for utdata hvis du ikke spesifiserer en annen fil.