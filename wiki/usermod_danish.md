# [Linux] Bash usermod brug: Administrer brugerkonti

## Oversigt
`usermod` kommandoen bruges til at ændre eksisterende brugerkonti på et Linux-system. Den giver systemadministratorer mulighed for at opdatere brugernavne, tilføje brugere til grupper, ændre hjemmemapper og meget mere.

## Brug
Den grundlæggende syntaks for `usermod` kommandoen er som følger:

```bash
usermod [muligheder] [brugernavn]
```

## Almindelige muligheder
- `-aG`: Tilføj brugeren til en eller flere grupper uden at fjerne dem fra andre grupper.
- `-d`: Angiv en ny hjemmemappe for brugeren.
- `-l`: Ændre brugernavnet.
- `-s`: Ændre brugerens login-shell.
- `-u`: Ændre brugerens UID (User ID).

## Almindelige eksempler

### Tilføj en bruger til en gruppe
For at tilføje brugeren `john` til gruppen `sudo`, kan du bruge følgende kommando:

```bash
usermod -aG sudo john
```

### Ændre brugernavn
For at ændre brugernavnet fra `john` til `johnny`, kan du bruge:

```bash
usermod -l johnny john
```

### Ændre hjemmemappe
For at ændre hjemmemappen for brugeren `john` til `/home/johnny`, kan du bruge:

```bash
usermod -d /home/johnny john
```

### Ændre login-shell
For at ændre login-shell for brugeren `john` til `/bin/bash`, kan du bruge:

```bash
usermod -s /bin/bash john
```

## Tips
- Sørg for at bruge `-aG` når du tilføjer brugere til grupper for at undgå at fjerne dem fra eksisterende grupper.
- Når du ændrer brugernavne, skal du være opmærksom på, at det kan påvirke filrettigheder og ejerskab.
- Det anbefales at tage en sikkerhedskopi af systemet, før du foretager ændringer med `usermod`, især i produktionsmiljøer.