# [Linux] Bash strace brug: Fejlfinding af systemopkald

## Oversigt
`strace` er et kraftfuldt værktøj, der bruges til at overvåge og diagnosticere systemopkald, som et program foretager. Det kan hjælpe udviklere og systemadministratorer med at forstå, hvordan programmer interagerer med kerne og systemressourcer.

## Brug
Den grundlæggende syntaks for `strace` er som følger:

```bash
strace [muligheder] [argumenter]
```

## Almindelige muligheder
- `-e trace=<type>`: Angiver, hvilke systemopkald der skal spores (f.eks. `file`, `network`).
- `-p <pid>`: Sporer et allerede kørende proces med det angivne proces-ID.
- `-o <fil>`: Gemmer output til en fil i stedet for at vise det på skærmen.
- `-c`: Giver en opsummering af systemopkald og deres tidsforbrug.
- `-f`: Følger forkede processer.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `strace` kan bruges:

### Spore et program
For at spore et program som `ls`, kan du køre:

```bash
strace ls
```

### Spore specifikke systemopkald
Hvis du kun vil spore filsystemopkald, kan du bruge:

```bash
strace -e trace=file ls
```

### Spore en kørende proces
For at spore en kørende proces med PID 1234:

```bash
strace -p 1234
```

### Gemme output til en fil
For at gemme output til en fil i stedet for at vise det på skærmen:

```bash
strace -o output.txt ls
```

### Opsummering af systemopkald
For at få en opsummering af systemopkald og deres tidsforbrug:

```bash
strace -c ls
```

## Tips
- Brug `-f` muligheden, hvis du vil følge forkede processer, som kan være nyttige i komplekse programmer.
- Overvej at gemme output til en fil med `-o`, så du kan analysere det senere.
- Vær opmærksom på, at `strace` kan påvirke programmets ydeevne, så det er bedst at bruge det i et testmiljø.