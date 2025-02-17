# [Linux] Bash nohup bruk: Kjør prosesser i bakgrunnen uten avbrudd

## Oversikt
`nohup` (no hang up) er et Bash-kommando som lar deg kjøre prosesser i bakgrunnen, selv om du logger ut fra terminalen. Dette er spesielt nyttig for langvarige oppgaver som du ønsker å fortsette å kjøre selv når du ikke er tilkoblet.

## Bruk
Grunnleggende syntaks for `nohup`-kommandoen er som følger:

```bash
nohup [alternativer] [argumenter] &
```

## Vanlige alternativer
- `&`: Kjør prosessen i bakgrunnen.
- `-h`: Vis hjelp for `nohup`.
- `-v`: Vis versjonsinformasjon.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `nohup`:

1. Kjør et skript i bakgrunnen:
   ```bash
   nohup ./mitt_skript.sh &
   ```

2. Kjør en Python-applikasjon i bakgrunnen:
   ```bash
   nohup python3 min_applikasjon.py &
   ```

3. Kjør en langvarig oppgave og send utdata til en fil:
   ```bash
   nohup long_running_command > output.log &
   ```

4. Kjør en prosess og ignorere standardfeil:
   ```bash
   nohup my_command > output.log 2>&1 &
   ```

## Tips
- Bruk `&` for å sikre at prosessen kjører i bakgrunnen.
- Sjekk `nohup.out`-filen for utdata hvis du ikke spesifiserer en utdatafil.
- Vær oppmerksom på at `nohup` ikke stopper prosessen hvis terminalen lukkes, så vær sikker på at du vil at prosessen skal fortsette å kjøre.