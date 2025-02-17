# [Linux] Bash printenv Bruk: Vise miljøvariabler

## Oversikt
`printenv`-kommandoen brukes til å vise miljøvariabler i Bash. Den gir en enkel måte å se hvilke variabler som er tilgjengelige i det nåværende miljøet, samt deres verdier.

## Bruk
Grunnleggende syntaks for `printenv`-kommandoen er som følger:

```bash
printenv [alternativer] [argumenter]
```

## Vanlige alternativer
- `-0`, `--null`: Skill variabler med null-tegn i stedet for linjeskift.
- `VARIABEL`: Angi navnet på en spesifikk miljøvariabel for å vise dens verdi.

## Vanlige eksempler
For å vise alle miljøvariabler:

```bash
printenv
```

For å vise verdien av en spesifikk miljøvariabel, for eksempel `HOME`:

```bash
printenv HOME
```

For å vise verdien av `PATH`-variabelen:

```bash
printenv PATH
```

For å vise miljøvariabler med null-tegn som skille:

```bash
printenv -0
```

## Tips
- Bruk `printenv` i kombinasjon med `grep` for å filtrere spesifikke variabler, for eksempel:

```bash
printenv | grep USER
```

- Hvis du ønsker å se alle miljøvariabler og deres verdier i en mer lesbar form, kan du bruke `env`-kommandoen som et alternativ:

```bash
env
```

- Vær oppmerksom på at `printenv` kun viser miljøvariabler, ikke lokale variabler definert i skript eller terminaløkten.