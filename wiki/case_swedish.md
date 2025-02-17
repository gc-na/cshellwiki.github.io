# [Linux] Bash case användning: Hantera mönsterbaserad matchning

## Översikt
`case`-kommandot i Bash används för att utföra mönsterbaserad matchning av variabler. Det är ett alternativ till flera `if`-satser och gör det enklare att hantera olika fall av en variabels värde.

## Användning
Den grundläggande syntaxen för `case`-kommandot ser ut så här:

```bash
case [variabel] in
    mönster1)
        # kommandon för mönster1
        ;;
    mönster2)
        # kommandon för mönster2
        ;;
    *)
        # kommandon för alla andra fall
        ;;
esac
```

## Vanliga alternativ
- `*)`: Detta är en "catch-all" som matchar alla värden som inte passar de angivna mönstren.
- `;;`: Markerar slutet på kommandona för ett specifikt mönster.

## Vanliga exempel

### Exempel 1: Enkel mönstermatchning
Detta exempel visar hur man använder `case` för att matcha en variabel mot olika alternativ.

```bash
#!/bin/bash
echo "Ange en siffra mellan 1 och 3:"
read nummer

case $nummer in
    1)
        echo "Du valde ett."
        ;;
    2)
        echo "Du valde två."
        ;;
    3)
        echo "Du valde tre."
        ;;
    *)
        echo "Ogiltigt val."
        ;;
esac
```

### Exempel 2: Filtypkontroll
Detta exempel kontrollerar filtypen baserat på filändelsen.

```bash
#!/bin/bash
filnamn="dokument.pdf"

case $filnamn in
    *.txt)
        echo "Detta är en textfil."
        ;;
    *.pdf)
        echo "Detta är en PDF-fil."
        ;;
    *.jpg|*.png)
        echo "Detta är en bildfil."
        ;;
    *)
        echo "Okänd filtyp."
        ;;
esac
```

### Exempel 3: Kommandoradsargument
Detta exempel visar hur man kan använda `case` för att hantera kommandoradsargument.

```bash
#!/bin/bash
case $1 in
    start)
        echo "Startar tjänsten."
        ;;
    stop)
        echo "Stoppar tjänsten."
        ;;
    restart)
        echo "Startar om tjänsten."
        ;;
    *)
        echo "Använd: start, stop eller restart."
        ;;
esac
```

## Tips
- Använd `case` när du har flera alternativ att kontrollera för en variabel, det gör koden mer läsbar.
- Kom ihåg att avsluta varje mönster med `;;` för att undvika oväntade beteenden.
- Du kan använda flera mönster för samma kommando genom att separera dem med `|`, som i exemplet med filtyper.