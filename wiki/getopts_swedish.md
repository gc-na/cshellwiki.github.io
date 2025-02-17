# [Linux] Bash getopts användning: Hantera kommandoradsalternativ

## Översikt
`getopts` är ett inbyggt Bash-kommando som används för att hantera kommandoradsalternativ och argument. Det gör det möjligt för skript att enkelt läsa och tolka flaggor och parametrar som ges av användaren.

## Användning
Den grundläggande syntaxen för `getopts` är:

```bash
getopts [options] [arguments]
```

## Vanliga alternativ
- `-a`: Används för att ange ett alternativ som ska tolkas.
- `-b`: Anger en flagga för ett specifikt beteende.
- `-c`: Används för att ange ett antal iterationer eller upprepningar.

## Vanliga exempel

### Exempel 1: Enkel användning av getopts
Detta exempel visar hur man använder `getopts` för att läsa en flagga och ett argument.

```bash
#!/bin/bash

while getopts "f:n:" opt; do
  case $opt in
    f) fil="$OPTARG"
    ;;
    n) namn="$OPTARG"
    ;;
    *) echo "Ogiltigt alternativ"; exit 1
    ;;
  esac
done

echo "Fil: $fil"
echo "Namn: $namn"
```

Körning:
```bash
./script.sh -f minfil.txt -n "John Doe"
```

### Exempel 2: Hantera flera alternativ
Detta exempel visar hur man kan hantera flera alternativ med `getopts`.

```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a) echo "Alternativ A aktiverat"
    ;;
    b) echo "Alternativ B med argument: $OPTARG"
    ;;
    c) echo "Alternativ C med argument: $OPTARG"
    ;;
    *) echo "Ogiltigt alternativ"; exit 1
    ;;
  esac
done
```

Körning:
```bash
./script.sh -a -b 123 -c "test"
```

## Tips
- Använd alltid `getopts` i en `while`-loop för att säkerställa att alla alternativ hanteras korrekt.
- Kom ihåg att `OPTARG` används för att hämta argumentet som följer ett alternativ.
- Testa alltid dina skript med olika kombinationer av alternativ för att se till att de fungerar som förväntat.