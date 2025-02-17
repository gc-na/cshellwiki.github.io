# [Linux] Bash xargs brug: Behandler input til kommandoer

## Oversigt
`xargs` er et kraftfuldt værktøj i Bash, der bruges til at konstruere og udføre kommandoer fra standard input. Det tager output fra en kommando og bruger det som argumenter til en anden kommando, hvilket gør det muligt at håndtere store mængder data effektivt.

## Brug
Den grundlæggende syntaks for `xargs` er som følger:

```bash
xargs [muligheder] [argumenter]
```

## Almindelige muligheder
- `-n N`: Angiver det maksimale antal argumenter, der skal sendes til kommandoen ad gangen.
- `-d DELIM`: Angiver en brugerdefineret delimiter i stedet for standard whitespace.
- `-I REPLACE`: Angiver en pladsholder, der skal erstattes med input fra standard input.
- `-p`: Spørger brugeren om bekræftelse, før hver kommando køres.
- `-0`: Behandler input som null-terminerede strenge, hvilket er nyttigt ved brug af `find` med `-print0`.

## Almindelige eksempler

### Eksempel 1: Slette filer
For at slette alle `.tmp` filer i en mappe kan du bruge:

```bash
find . -name "*.tmp" | xargs rm
```

### Eksempel 2: Begrænsning af argumenter
Hvis du kun vil sende 5 filer ad gangen til `rm`, kan du gøre det således:

```bash
find . -name "*.log" | xargs -n 5 rm
```

### Eksempel 3: Brugerdefineret delimiter
Hvis du har en liste over filnavne adskilt af semikolon, kan du bruge:

```bash
echo "file1.txt;file2.txt;file3.txt" | xargs -d ';' rm
```

### Eksempel 4: Bekræftelse før sletning
For at bekræfte før hver sletning kan du bruge:

```bash
find . -name "*.bak" | xargs -p rm
```

## Tips
- Brug `-0` sammen med `find` og `-print0` for at undgå problemer med filnavne, der indeholder mellemrum.
- Vær forsigtig med `rm`-kommandoen og test først med `echo` for at se, hvilke filer der vil blive påvirket.
- Overvej at bruge `-I` til at tilpasse, hvordan input placeres i kommandoen, hvis du har brug for mere kontrol over argumenterne.