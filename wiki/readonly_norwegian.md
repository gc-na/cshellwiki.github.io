# [Linux] Bash readonly bruken: Gjør variabler skrivebeskyttede

## Oversikt
`readonly`-kommandoen i Bash brukes til å gjøre variabler skrivebeskyttede, noe som betyr at verdien av en variabel ikke kan endres etter at den er blitt erklært som readonly. Dette er nyttig for å forhindre utilsiktede endringer i viktige variabler i skriptene dine.

## Bruk
Den grunnleggende syntaksen for `readonly`-kommandoen er:

```bash
readonly [variabelnavn[=verdi]]
```

## Vanlige alternativer
- `-p`: Viser en liste over alle skrivebeskyttede variabler i gjeldende miljø.

## Vanlige eksempler

### Eksempel 1: Opprette en skrivebeskyttet variabel
```bash
readonly MY_VAR="Dette er en skrivebeskyttet variabel"
```

### Eksempel 2: Forsøke å endre en skrivebeskyttet variabel
```bash
MY_VAR="Prøver å endre"  # Dette vil gi en feilmelding
```

### Eksempel 3: Vise alle skrivebeskyttede variabler
```bash
readonly -p
```

## Tips
- Bruk `readonly` for variabler som inneholder konfigurasjonsverdier eller viktige innstillinger som ikke skal endres.
- Vær oppmerksom på at `readonly` kun gjelder for den aktuelle shell-økten; når du lukker terminalvinduet, vil innstillingene gå tapt.
- Du kan bruke `declare -r` som et alternativ til `readonly` for å oppnå samme effekt.