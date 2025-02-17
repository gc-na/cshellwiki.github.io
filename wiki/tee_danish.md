# [Linux] Bash tee brug: [kopier og skriv til fil]

## Oversigt
`tee`-kommandoen i Bash bruges til at læse fra standard input og skrive til både standard output og en eller flere filer. Dette gør det muligt at se output fra en kommando, mens det samtidig gemmes i en fil.

## Brug
Den grundlæggende syntaks for `tee`-kommandoen er:

```bash
tee [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`, `--append`: Tilføj output til slutningen af filen i stedet for at overskrive den.
- `-i`, `--ignore-interrupts`: Ignorerer signaler, der kan stoppe kommandoen.
- `--version`: Vis versionen af `tee`.

## Almindelige eksempler

### Eksempel 1: Grundlæggende brug
For at gemme output fra en kommando i en fil, kan du bruge:

```bash
echo "Hej verden" | tee fil.txt
```

Dette vil skrive "Hej verden" til både terminalen og `fil.txt`.

### Eksempel 2: Tilføje til en fil
Hvis du vil tilføje output til en eksisterende fil, kan du bruge `-a`:

```bash
echo "Ny linje" | tee -a fil.txt
```

Dette tilføjer "Ny linje" til slutningen af `fil.txt` uden at slette eksisterende indhold.

### Eksempel 3: Skrive til flere filer
Du kan også skrive output til flere filer samtidig:

```bash
echo "Data gemmes" | tee fil1.txt fil2.txt
```

Dette vil skrive "Data gemmes" til både `fil1.txt` og `fil2.txt`.

## Tips
- Brug `tee` i kombination med andre kommandoer for at gemme output, mens du stadig ser det. For eksempel: `dmesg | tee log.txt`.
- Vær opmærksom på, at hvis du ikke bruger `-a`, vil `tee` overskrive indholdet af filen, hvis den allerede eksisterer.
- `tee` kan være nyttigt i scripts, hvor du vil logge output fra en proces til senere analyse.