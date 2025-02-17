# [Linux] Bash if användning: Kontrollera villkor

## Översikt
`if`-kommandot i Bash används för att utföra kommandon baserat på om ett visst villkor är sant eller falskt. Det är en grundläggande del av skriptprogrammering och gör det möjligt att styra flödet av programmet.

## Användning
Den grundläggande syntaxen för `if`-kommandot är:

```bash
if [ villkor ]; then
    # kommandon att köra om villkoret är sant
fi
```

## Vanliga alternativ
- `-e`: Kontrollerar om en fil existerar.
- `-d`: Kontrollerar om en katalog existerar.
- `-f`: Kontrollerar om en fil är en vanlig fil.
- `-z`: Kontrollerar om en sträng är tom.
- `==`: Jämför två strängar för likhet.

## Vanliga exempel

### Exempel 1: Kontrollera om en fil finns
```bash
if [ -e "minfil.txt" ]; then
    echo "Filen finns."
else
    echo "Filen finns inte."
fi
```

### Exempel 2: Kontrollera om en katalog finns
```bash
if [ -d "minkatalog" ]; then
    echo "Katalogen finns."
else
    echo "Katalogen finns inte."
fi
```

### Exempel 3: Jämföra två strängar
```bash
str1="hej"
str2="hej"
if [ "$str1" == "$str2" ]; then
    echo "Strängarna är lika."
else
    echo "Strängarna är inte lika."
fi
```

### Exempel 4: Kontrollera om en variabel är tom
```bash
variabel=""
if [ -z "$variabel" ]; then
    echo "Variabeln är tom."
else
    echo "Variabeln har ett värde."
fi
```

## Tips
- Använd alltid citattecken runt variabler för att undvika problem med tomma värden.
- Se till att använda mellanslag korrekt runt hakparenteser för att undvika syntaxfel.
- Kombinera flera villkor med `&&` (och) eller `||` (eller) för mer komplex logik.