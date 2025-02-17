# [Linux] Bash getopts Bruk: Håndtering av kommandolinjealternativer

## Oversikt
`getopts` er et innebygd Bash-verktøy som brukes til å analysere kommandolinjealternativer og argumenter. Det gjør det enklere å håndtere flagg og parametere i skriptene dine, noe som gir en mer strukturert og brukervennlig tilnærming til kommandolinjegrensesnitt.

## Bruk
Den grunnleggende syntaksen for `getopts` er som følger:

```bash
getopts [options] [arguments]
```

## Vanlige alternativer
- `-a`: Angir at `getopts` skal håndtere flere alternativer.
- `-o`: Brukes til å spesifisere hvilke alternativer som skal aksepteres.
- `-l`: Brukes for lange alternativer (navn).

## Vanlige eksempler

### Eksempel 1: Enkel bruk av getopts
Her er et enkelt skript som bruker `getopts` for å håndtere to alternativer: `-a` og `-b`.

```bash
#!/bin/bash

while getopts "ab" option; do
  case $option in
    a) echo "Alternativ A valgt";;
    b) echo "Alternativ B valgt";;
    *) echo "Ugyldig alternativ";;
  esac
done
```

### Eksempel 2: Alternativer med argumenter
I dette eksemplet håndterer vi et alternativ som krever et argument.

```bash
#!/bin/bash

while getopts "n:" option; do
  case $option in
    n) echo "Navn: $OPTARG";;
    *) echo "Ugyldig alternativ";;
  esac
done
```

### Eksempel 3: Flere alternativer
Her er et skript som håndterer flere alternativer og argumenter.

```bash
#!/bin/bash

while getopts "a:b:c:" option; do
  case $option in
    a) echo "Alternativ A med verdi: $OPTARG";;
    b) echo "Alternativ B med verdi: $OPTARG";;
    c) echo "Alternativ C med verdi: $OPTARG";;
    *) echo "Ugyldig alternativ";;
  esac
done
```

## Tips
- Husk å bruke `OPTIND` for å tilbakestille indeksen for alternativer hvis du bruker `getopts` flere ganger i samme skript.
- Bruk `:` etter et alternativ for å indikere at det krever et argument.
- For lange alternativer, vurder å bruke `getopt` i stedet for `getopts` for mer kompleks håndtering.