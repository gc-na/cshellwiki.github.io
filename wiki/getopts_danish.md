# [Linux] Bash getopts brug: Håndtering af kommandolinjeparametre

## Oversigt
`getopts` er et indbygget Bash-kommando, der bruges til at analysere og håndtere kommandolinjeparametre i scripts. Det gør det muligt at definere og fortolke indstillinger og argumenter, hvilket gør scripts mere fleksible og brugervenlige.

## Brug
Den grundlæggende syntaks for `getopts` er som følger:

```bash
getopts [options] [arguments]
```

## Almindelige muligheder
- `-a`: Angiver, at argumenter skal behandles som en liste.
- `-b`: Bruges til at aktivere en specifik funktion i scriptet.
- `-c`: Tager et argument, der angiver en konfiguration.
- `-h`: Viser hjælp og brugervejledning.
- `-v`: Aktiverer detaljeret uddata (verbose mode).

## Almindelige eksempler

### Eksempel 1: Grundlæggende brug af getopts
Dette eksempel viser, hvordan man bruger `getopts` til at håndtere enkle muligheder.

```bash
#!/bin/bash

while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Option A valgt"
      ;;
    b)
      echo "Option B valgt med argument: $OPTARG"
      ;;
    c)
      echo "Option C valgt"
      ;;
    *)
      echo "Ugyldig option"
      ;;
  esac
done
```

### Eksempel 2: Brug af getopts med flere argumenter
I dette eksempel håndteres flere argumenter og muligheder.

```bash
#!/bin/bash

while getopts "x:y:z:" opt; do
  case $opt in
    x)
      echo "Option X valgt med argument: $OPTARG"
      ;;
    y)
      echo "Option Y valgt med argument: $OPTARG"
      ;;
    z)
      echo "Option Z valgt med argument: $OPTARG"
      ;;
    *)
      echo "Ugyldig option"
      ;;
  esac
done
```

### Eksempel 3: Vise hjælp
Her er et eksempel på, hvordan man implementerer en hjælpemulighed.

```bash
#!/bin/bash

while getopts "h" opt; do
  case $opt in
    h)
      echo "Brug: script.sh [-a] [-b argument] [-c]"
      exit 0
      ;;
    *)
      echo "Ugyldig option"
      ;;
  esac
done
```

## Tips
- Sørg for at inkludere en hjælpemulighed i dit script, så brugerne kan forstå, hvordan de skal bruge det.
- Brug `OPTARG` til at få adgang til argumenter, der følger efter en mulighed.
- Test dit script med forskellige kombinationer af muligheder for at sikre, at det håndterer alle scenarier korrekt.