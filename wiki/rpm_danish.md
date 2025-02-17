# [Linux] Bash rpm brug: Administrer RPM-pakker

## Oversigt
`rpm` (Red Hat Package Manager) er et kommandolinjeværktøj, der bruges til at installere, opdatere, fjerne og administrere RPM-pakker på Linux-systemer. Det er især populært på distributioner som Red Hat, Fedora og CentOS.

## Brug
Den grundlæggende syntaks for `rpm`-kommandoen er:

```bash
rpm [options] [arguments]
```

## Almindelige muligheder
- `-i`: Installer en RPM-pakke.
- `-e`: Fjern en installeret RPM-pakke.
- `-U`: Opdater en RPM-pakke, hvis den allerede er installeret.
- `-q`: Spørg om en installeret pakke.
- `-l`: Vis filerne, der er inkluderet i en installeret pakke.
- `--checksig`: Kontroller signaturen af en RPM-pakke.

## Almindelige eksempler

### Installere en RPM-pakke
For at installere en RPM-pakke kan du bruge følgende kommando:

```bash
rpm -i pakke.rpm
```

### Opdatere en RPM-pakke
Hvis du vil opdatere en eksisterende pakke, kan du bruge:

```bash
rpm -U pakke.rpm
```

### Fjerne en RPM-pakke
For at fjerne en installeret pakke, brug:

```bash
rpm -e pakke-navn
```

### Spørge om en installeret pakke
For at finde ud af, om en pakke er installeret, og få dens version, kan du køre:

```bash
rpm -q pakke-navn
```

### Liste filer i en installeret pakke
For at se, hvilke filer der er inkluderet i en installeret pakke, kan du bruge:

```bash
rpm -l pakke-navn
```

## Tips
- Sørg for at have de nødvendige rettigheder (ofte som root) for at installere eller fjerne pakker.
- Brug `--checksig` for at sikre, at pakken er autentisk, før du installerer den.
- Hold dine pakker opdaterede for at sikre, at du har de nyeste sikkerhedsopdateringer og funktioner.