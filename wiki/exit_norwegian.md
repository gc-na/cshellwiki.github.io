# [Linux] Bash exit bruk: Avslutt et skript eller en terminaløkt

## Oversikt
`exit`-kommandoen brukes i Bash for å avslutte et skript eller en terminaløkt. Den kan også returnere en statuskode som indikerer om skriptet ble fullført vellykket eller om det oppstod en feil.

## Bruk
Den grunnleggende syntaksen for `exit`-kommandoen er som følger:

```bash
exit [statuskode]
```

## Vanlige alternativer
- `statuskode`: En valgfri heltallsverdi som angir avslutningsstatus. Standardverdi er 0, som indikerer suksess. Enhver annen verdi indikerer en feil.

## Vanlige eksempler

### Eksempel 1: Avslutte et skript
For å avslutte et skript med suksess:

```bash
#!/bin/bash
echo "Skriptet kjører..."
exit 0
```

### Eksempel 2: Avslutte med en feilstatus
For å avslutte et skript med en feilkode:

```bash
#!/bin/bash
echo "Noe gikk galt!"
exit 1
```

### Eksempel 3: Bruke exit i en interaktiv terminal
Du kan også bruke `exit` i en interaktiv terminal for å avslutte økten:

```bash
exit
```

## Tips
- Bruk alltid `exit 0` for å indikere at skriptet har kjørt uten feil.
- Hvis du bruker `exit` i en funksjon, vil det avslutte hele skriptet, ikke bare funksjonen.
- Vær oppmerksom på at terminalen vil lukke seg hvis du bruker `exit` uten å være i et skript.