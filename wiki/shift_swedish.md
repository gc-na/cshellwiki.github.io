# [Linux] Bash shift användning: Flytta positionen av argument

## Översikt
`shift` är ett Bash-kommando som används för att flytta positionen av argument i ett skript. När du använder `shift` flyttas alla argument ett steg åt vänster, vilket innebär att det första argumentet tas bort och de efterföljande argumenten flyttas upp i listan.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
shift [n]
```

Där `n` är det antal positioner som argumenten ska flyttas. Om `n` inte anges, flyttas argumenten ett steg.

## Vanliga alternativ
- `n`: Anger hur många positioner argumenten ska flyttas. Om inget värde anges, flyttas argumenten ett steg.

## Vanliga exempel
Här är några praktiska exempel på hur `shift` kan användas:

### Exempel 1: Grundläggande användning
Flytta argumenten ett steg åt vänster:

```bash
#!/bin/bash
echo "Första argumentet: $1"
shift
echo "Efter shift, första argumentet: $1"
```

### Exempel 2: Flytta flera positioner
Flytta argumenten två steg åt vänster:

```bash
#!/bin/bash
echo "Första argumentet: $1"
echo "Andra argumentet: $2"
shift 2
echo "Efter shift, första argumentet: $1"
```

### Exempel 3: Använda i en loop
Använd `shift` för att bearbeta alla argument i en loop:

```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "Bearbetar argument: $1"
    shift
done
```

## Tips
- Använd `shift` i skript där du behöver bearbeta en lista med argument sekventiellt.
- Var försiktig med att använda `shift` för många gånger; om du försöker flytta mer än antalet tillgängliga argument kommer `$1` att bli tomt.
- Kombinera `shift` med andra kommandon som `case` eller `if` för att skapa mer dynamiska skript.