# [Linux] Bash iotop bruk: overvåk disk I/O i sanntid

## Oversikt
iotop er et verktøy for å overvåke disk I/O (input/output) i sanntid på Linux-systemer. Det gir en visuell fremstilling av hvilke prosesser som bruker mest diskressurser, noe som kan være nyttig for feilsøking og ytelsesoptimalisering.

## Bruk
Den grunnleggende syntaksen for iotop er:

```bash
iotop [alternativer] [argumenter]
```

## Vanlige alternativer
- `-o`, `--only`: Vis bare prosesser som for øyeblikket utfører I/O.
- `-b`, `--batch`: Kjør iotop i batch-modus, noe som betyr at den ikke vil vise en interaktiv skjerm.
- `-n NUM`, `--iter=NUM`: Angi hvor mange ganger iotop skal oppdatere visningen før den avslutter.
- `-d SEC`, `--delay=SEC`: Sett oppdateringsfrekvensen i sekunder.

## Vanlige eksempler
For å starte iotop og vise prosesser som bruker I/O:

```bash
sudo iotop
```

For å vise bare prosesser som for øyeblikket utfører I/O:

```bash
sudo iotop -o
```

For å kjøre iotop i batch-modus og oppdatere visningen 5 ganger med 2 sekunders intervall:

```bash
sudo iotop -b -n 5 -d 2
```

## Tips
- Kjør iotop med `sudo` for å få tilgang til all nødvendig informasjon om prosessene.
- Bruk `-o` alternativet for å fokusere på prosesser som faktisk bruker I/O, noe som kan gjøre det lettere å identifisere problemer.
- Vær oppmerksom på at iotop kan ha en viss overhead, så det er best å bruke det i situasjoner der du aktivt feilsøker I/O-problemer.