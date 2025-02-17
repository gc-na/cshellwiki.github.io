# [Linux] Bash usermod bruken: Endre brukerinnstillinger

## Oversikt
`usermod` er et Bash-kommando som brukes til å endre egenskaper og innstillinger for eksisterende brukerkontoer på et Linux-system. Dette kan inkludere endring av brukerens gruppe, hjemmekatalog, skall, og mer.

## Bruk
Grunnleggende syntaks for `usermod`-kommandoen er som følger:

```bash
usermod [alternativer] [argumenter]
```

## Vanlige alternativer
- `-aG`: Legg til brukeren i en eller flere grupper uten å fjerne dem fra andre grupper.
- `-d`: Endre brukerens hjemmekatalog.
- `-s`: Endre brukerens skall.
- `-L`: Låse kontoen til brukeren.
- `-U`: Låse opp kontoen til brukeren.

## Vanlige eksempler

### Legge til en bruker i en gruppe
For å legge til brukeren `ole` i gruppen `sudo`, kan du bruke følgende kommando:

```bash
usermod -aG sudo ole
```

### Endre hjemmekatalog
For å endre hjemmekatalogen til brukeren `kari` til `/home/kari_new`, kan du bruke:

```bash
usermod -d /home/kari_new kari
```

### Endre skall
For å endre skall for brukeren `per` til `/bin/zsh`, kan du bruke:

```bash
usermod -s /bin/zsh per
```

### Låse en konto
For å låse kontoen til brukeren `anna`, kan du bruke:

```bash
usermod -L anna
```

### Låse opp en konto
For å låse opp kontoen til brukeren `anna`, kan du bruke:

```bash
usermod -U anna
```

## Tips
- Sørg for å bruke `usermod` med administrative rettigheter, vanligvis som root eller med `sudo`.
- Vær forsiktig når du endrer grupper, da det kan påvirke brukerens tilgang til filer og ressurser.
- Etter å ha endret skall, kan det være nødvendig å logge ut og inn igjen for at endringene skal tre i kraft.