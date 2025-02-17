# [Linux] Bash iotop brug: Overvåg disk I/O i realtid

## Oversigt
iotop er et værktøj til at overvåge disk I/O (Input/Output) i realtid. Det viser, hvilke processer der bruger mest diskressourcer, hvilket kan være nyttigt til fejlfinding af ydeevneproblemer på systemet.

## Brug
Den grundlæggende syntaks for iotop er:

```bash
iotop [muligheder] [argumenter]
```

## Almindelige muligheder
- `-o`, `--only`: Vis kun processer, der bruger I/O.
- `-b`, `--batch`: Kør i batch-tilstand, hvilket gør det muligt at sende output til en fil.
- `-d`, `--delay`: Angiv forsinkelse mellem opdateringer (i sekunder).
- `-p`, `--pid`: Overvåg kun en specifik proces ved at angive dens PID.

## Almindelige eksempler
For at starte iotop og se alle processer, der bruger disk I/O, kan du bruge:

```bash
sudo iotop
```

For kun at vise processer, der aktivt bruger I/O, kan du køre:

```bash
sudo iotop -o
```

Hvis du ønsker at køre iotop i batch-tilstand med en opdateringsfrekvens på 5 sekunder, kan du bruge:

```bash
sudo iotop -b -d 5
```

For at overvåge en specifik proces med PID 1234, kan du køre:

```bash
sudo iotop -p 1234
```

## Tips
- Kør iotop med `sudo` for at få de mest præcise oplysninger om alle processer.
- Brug `-d` til at justere opdateringsfrekvensen, så den passer til dine behov.
- Overvåg iotop i batch-tilstand, hvis du vil gemme output til analyse senere.