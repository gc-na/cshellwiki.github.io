# [Linux] Bash rm brug: Slet filer og mapper

## Oversigt
`rm`-kommandoen bruges til at slette filer og mapper i Unix-lignende operativsystemer. Det er en kraftfuld kommando, der kan fjerne filer permanent, så det er vigtigt at bruge den med forsigtighed.

## Brug
Den grundlæggende syntaks for `rm`-kommandoen er:

```bash
rm [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`: Tvinger sletning uden at spørge om bekræftelse.
- `-i`: Spørger om bekræftelse, før hver fil slettes.
- `-r`: Sletter mapper rekursivt, inklusive deres indhold.
- `-v`: Viser detaljer om, hvad der bliver slettet.

## Almindelige eksempler
Slet en enkelt fil:

```bash
rm filnavn.txt
```

Slet flere filer på én gang:

```bash
rm fil1.txt fil2.txt fil3.txt
```

Slet en mappe og dens indhold rekursivt:

```bash
rm -r mappe/
```

Slet en fil uden at blive spurgt om bekræftelse:

```bash
rm -f filnavn.txt
```

Slet en fil med bekræftelse for hver fil:

```bash
rm -i filnavn.txt
```

## Tips
- Brug `-i`-muligheden, når du sletter vigtige filer, for at undgå utilsigtet sletning.
- Tjek altid filnavne og stier, før du kører `rm`, især med `-r` og `-f` mulighederne.
- Overvej at bruge `trash-cli` eller lignende værktøjer, hvis du ønsker en "papirkurv"-funktionalitet, så du kan gendanne filer, hvis det er nødvendigt.