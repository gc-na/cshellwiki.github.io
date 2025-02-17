# [Linux] Bash who brug: Vis brugere der er logget ind

## Oversigt
`who`-kommandoen viser en liste over brugere, der i øjeblikket er logget ind på systemet. Det giver information om, hvornår de loggede ind, og hvilken terminal de bruger.

## Brug
Den grundlæggende syntaks for `who`-kommandoen er:

```bash
who [options] [arguments]
```

## Almindelige muligheder
- `-a`: Viser alle tilgængelige oplysninger om brugerne, inklusive inaktive brugere.
- `-b`: Viser tidspunktet for den seneste systemopstart.
- `-q`: Viser kun brugernavne og antallet af loggede brugere.
- `--help`: Viser hjælp til brug af kommandoen.

## Almindelige eksempler
For at se en liste over alle loggede brugere, kan du bruge:

```bash
who
```

For at se alle detaljerede oplysninger om brugerne, kan du bruge:

```bash
who -a
```

Hvis du kun vil se antallet af loggede brugere, kan du køre:

```bash
who -q
```

For at finde ud af, hvornår systemet sidst blev startet, kan du bruge:

```bash
who -b
```

## Tips
- Brug `who` i kombination med `grep` for at filtrere specifikke brugernavne. For eksempel: 

```bash
who | grep username
```

- Overvej at bruge `w`-kommandoen, hvis du også vil se, hvad de loggede brugere laver i øjeblikket.
- Tjek regelmæssigt, hvem der er logget ind, for at sikre, at der ikke er uautoriserede brugere på systemet.