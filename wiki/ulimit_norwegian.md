# [Linux] Bash ulimit bruk: Juster ressursgrenser for prosesser

## Oversikt
`ulimit`-kommandoen brukes i Bash for å sette eller vise ressursgrenser for prosesser som kjøres i den nåværende shell-økten. Dette kan være nyttig for å forhindre at prosesser bruker for mange systemressurser, noe som kan påvirke systemets stabilitet og ytelse.

## Bruk
Grunnleggende syntaks for `ulimit`-kommandoen er som følger:

```bash
ulimit [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser alle ressursgrenser.
- `-c`: Setter grensen for størrelsen på kjernedumpfiler.
- `-d`: Setter grensen for størrelsen på datasegmentet.
- `-f`: Setter grensen for størrelsen på filer som kan opprettes.
- `-l`: Setter grensen for størrelsen på låste minnesider.
- `-m`: Setter grensen for størrelsen på fysisk minne.
- `-n`: Setter grensen for antall åpne filer.
- `-s`: Setter stakken størrelse.
- `-t`: Setter grensen for CPU-tid i sekunder.

## Vanlige eksempler

### Vise alle ressursgrenser
For å vise alle gjeldende ressursgrenser, kan du bruke:

```bash
ulimit -a
```

### Sett grensen for antall åpne filer
For å sette grensen for antall åpne filer til 1024, kan du bruke:

```bash
ulimit -n 1024
```

### Sett grensen for maksimal størrelse på kjernedumpfil
For å sette grensen for størrelsen på kjernedumpfiler til 0 (deaktiver kjernedump), kan du bruke:

```bash
ulimit -c 0
```

### Sett stakkstørrelse
For å sette stakkstørrelsen til 8 MB, kan du bruke:

```bash
ulimit -s 8192
```

## Tips
- Vær oppmerksom på at endringer gjort med `ulimit` kun gjelder for den nåværende shell-økten og vil ikke påvirke andre prosesser eller shell-økter.
- For å gjøre permanente endringer, kan du legge til `ulimit`-innstillinger i konfigurasjonsfilene som `~/.bashrc` eller `/etc/security/limits.conf`.
- Bruk `ulimit -a` for å sjekke gjeldende innstillinger før du gjør endringer, slik at du vet hva som er satt fra før.