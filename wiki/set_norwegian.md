# [Linux] Bash set bruk: Endre shell-innstillinger

## Oversikt
`set`-kommandoen i Bash brukes til å endre innstillinger for shell-miljøet. Den lar brukeren aktivere eller deaktivere spesifikke funksjoner og kontrollere hvordan skript og interaktive shell fungerer.

## Bruk
Grunnleggende syntaks for `set`-kommandoen er som følger:

```bash
set [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e`: Avslutt skriptet hvis en kommando feiler.
- `-u`: Behandle ubestemte variabler som feil.
- `-x`: Aktiverer sporing, viser kommandoer før de kjøres.
- `-o`: Setter spesifikke shell-alternativer, som `-o noclobber` for å forhindre overskriving av filer.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `set`-kommandoen:

### Eksempel 1: Avslutt ved feil
```bash
set -e
kommando_som_kan_feile
echo "Denne meldingen vises ikke hvis kommandoen feiler."
```

### Eksempel 2: Behandle ubestemte variabler
```bash
set -u
echo $UBESTEMT_VAR
```
Dette vil gi en feil hvis `UBESTEMT_VAR` ikke er definert.

### Eksempel 3: Aktiver sporing
```bash
set -x
echo "Sporing aktivert"
```
Dette vil vise kommandoene som kjøres i terminalen.

### Eksempel 4: Kombinere alternativer
```bash
set -eu
echo "Skriptet vil avslutte ved feil og behandle ubestemte variabler."
```

## Tips
- Bruk `set -e` i skript for å sikre at feil ikke blir ignorert.
- Aktiver `set -x` under feilsøking for å se hva som skjer i skriptet.
- Husk å tilbakestille innstillinger etter bruk, hvis nødvendig, for å unngå uventede atferder i etterfølgende kommandoer.