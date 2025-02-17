# [Linux] Bash trap brug: Håndtering af signaler og afslutning

## Oversigt
`trap`-kommandoen i Bash bruges til at fange og håndtere signaler og hændelser, der opstår under udførelsen af et script. Dette gør det muligt at udføre specifik kode, når et bestemt signal modtages, hvilket kan være nyttigt til at rydde op eller afslutte processer korrekt.

## Brug
Den grundlæggende syntaks for `trap`-kommandoen er som følger:

```bash
trap [handling] [signal]
```

Her specificerer `[handling]` den kommando eller det script, der skal udføres, når det angivne `[signal]` modtages.

## Almindelige muligheder
- `SIGINT`: Signal sendt ved Ctrl+C, typisk brugt til at stoppe et script.
- `SIGTERM`: Signal sendt for at anmode om, at et program afsluttes.
- `EXIT`: Signal, der aktiveres, når scriptet afsluttes, uanset årsagen.
- `ERR`: Signal, der aktiveres, når en kommando i scriptet fejler.

## Almindelige eksempler

### Eksempel 1: Håndtering af SIGINT
Dette eksempel viser, hvordan man fanger Ctrl+C og udfører en oprydningsfunktion.

```bash
#!/bin/bash

trap 'echo "Afslutter script..."; exit' SIGINT

while true; do
    echo "Kører... Tryk Ctrl+C for at afslutte."
    sleep 1
done
```

### Eksempel 2: Rydde op ved afslutning
Her fanges EXIT-signalet for at udføre oprydning, når scriptet afsluttes.

```bash
#!/bin/bash

trap 'echo "Rydder op..."; rm -f temp.txt' EXIT

echo "Opretter midlertidig fil..."
touch temp.txt
```

### Eksempel 3: Håndtering af fejl
Dette eksempel viser, hvordan man kan håndtere fejl ved at fange ERR-signalet.

```bash
#!/bin/bash

trap 'echo "Der opstod en fejl!"' ERR

echo "Kører en kommando, der fejler..."
false  # Denne kommando fejler
echo "Denne linje vil ikke blive udført."
```

## Tips
- Brug `trap` til at sikre, at ressourcer frigives korrekt, når et script afsluttes.
- Test dine `trap`-kommandoer grundigt for at sikre, at de fungerer som forventet under forskellige scenarier.
- Overvej at bruge `trap` i kombination med funktioner for at holde din kode organiseret og let at vedligeholde.