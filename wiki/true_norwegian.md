# [Linux] Bash true bruken: Alltid sann

## Oversikt
`true` er en enkel Bash-kommando som alltid returnerer en exit-status på 0, noe som indikerer suksess. Den brukes ofte i skript for å opprettholde syntaksen eller som en plassholder der en kommando kreves, men ingen handling er nødvendig.

## Bruk
Den grunnleggende syntaksen for `true` er:

```bash
true [alternativer] [argumenter]
```

## Vanlige alternativer
`true` har ingen spesifikke alternativer, da dens eneste funksjon er å returnere en suksessstatus. 

## Vanlige eksempler

### Eksempel 1: Enkel bruk
For å bruke `true` i terminalen, kan du ganske enkelt skrive:

```bash
true
```

Dette vil ikke gi noe utdata, men exit-statusen vil være 0.

### Eksempel 2: Bruke true i en if-setning
Du kan bruke `true` i en if-setning for å alltid utføre en blokk med kode:

```bash
if true; then
    echo "Dette vil alltid bli skrevet ut."
fi
```

### Eksempel 3: Som en plassholder i skript
Når du skriver skript og ønsker å ha en plassholder for fremtidige kommandoer, kan `true` brukes:

```bash
#!/bin/bash

# Plassholder for fremtidig kode
true

echo "Koden fortsetter her."
```

## Tips
- Bruk `true` i skript for å unngå feil i syntaks når du trenger en kommando som alltid lykkes.
- Det kan være nyttig å bruke `true` i kombinasjon med `&&` for å kjøre flere kommandoer betinget på suksess.
- Husk at `true` ikke gir noe utdata, så hvis du trenger tilbakemelding, må du bruke `echo` eller en annen kommando.