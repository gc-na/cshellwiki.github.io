# [Linux] Bash else användning: Används för att specificera alternativ i skript

## Översikt
`else` är en kontrollstruktur i Bash som används för att ange ett alternativ som ska utföras om det föregående villkoret (definierat med `if`) inte är sant. Det är en viktig del av flödeskontrollen i skript, vilket gör det möjligt att hantera olika scenarier baserat på villkor.

## Användning
Den grundläggande syntaxen för `else` ser ut som följer:

```bash
if [ villkor ]; then
    # kommandon om villkoret är sant
else
    # kommandon om villkoret är falskt
fi
```

## Vanliga alternativ
`else` har inga specifika alternativ, men det används ofta tillsammans med `if` och `elif` för att skapa komplexa villkorssatser.

## Vanliga exempel

### Exempel 1: Enkel if-else
Detta exempel visar hur man använder `else` för att hantera ett enkelt villkor.

```bash
#!/bin/bash
num=10

if [ $num -gt 5 ]; then
    echo "Numret är större än 5."
else
    echo "Numret är 5 eller mindre."
fi
```

### Exempel 2: Kontroll av filens existens
I detta exempel används `else` för att kontrollera om en fil finns.

```bash
#!/bin/bash
fil="minfil.txt"

if [ -e $fil ]; then
    echo "Filen finns."
else
    echo "Filen finns inte."
fi
```

### Exempel 3: Använda else med elif
Här används `else` tillsammans med `elif` för att hantera flera villkor.

```bash
#!/bin/bash
tal=7

if [ $tal -gt 10 ]; then
    echo "Talet är större än 10."
elif [ $tal -eq 10 ]; then
    echo "Talet är lika med 10."
else
    echo "Talet är mindre än 10."
fi
```

## Tips
- Använd alltid `fi` för att avsluta en `if`-struktur, inklusive `else`.
- För att förbättra läsbarheten, indentera kommandon under `if`, `elif` och `else`.
- Testa alltid dina skript med olika ingångsvärden för att säkerställa att alla villkor hanteras korrekt.