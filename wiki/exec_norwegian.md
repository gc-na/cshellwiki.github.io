# [Linux] Bash exec bruk: Kjør et kommando i gjeldende skall

## Oversikt
`exec`-kommandoen i Bash brukes til å erstatte den nåværende prosessen med en ny prosess. Dette betyr at når du kjører en kommando med `exec`, vil den nåværende skallprosessen bli avsluttet, og den nye kommandoen vil ta over. Dette kan være nyttig for å spare ressurser eller for å endre skallmiljøet.

## Bruk
Den grunnleggende syntaksen for `exec`-kommandoen er:

```bash
exec [alternativer] [kommando] [argumenter]
```

## Vanlige alternativer
- `-a` : Angi et annet navn for den nye prosessen.
- `-l` : Gjør at den nye prosessen blir en login-shell.
- `-c` : Kjør kommandoen i en ny skallprosess.

## Vanlige eksempler

### Erstatte skall med et nytt program
For å erstatte det nåværende skallvinduet med `bash`, kan du bruke:

```bash
exec bash
```

### Kjør et skript og erstatte gjeldende skall
Hvis du har et skript som heter `script.sh`, kan du kjøre det med:

```bash
exec ./script.sh
```

### Bruke exec med et annet prosessnavn
For å kjøre `ls`-kommandoen og gi den et annet prosessnavn, kan du bruke:

```bash
exec -a nytt_navn ls -l
```

### Kjør en kommando i en ny skallprosess
For å kjøre en kommando i en ny skallprosess, kan du bruke:

```bash
exec sh -c 'echo Hello World'
```

## Tips
- Vær oppmerksom på at når du bruker `exec`, vil det nåværende skallvinduet bli avsluttet, så vær sikker på at du ønsker å erstatte det.
- Bruk `exec` når du vil spare ressurser, spesielt i skript der du ikke trenger å gå tilbake til det opprinnelige skallet.
- Test kommandoene dine i et sikkert miljø før du bruker `exec` i produksjon, for å unngå utilsiktede konsekvenser.