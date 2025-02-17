# [Linux] Bash case gebruik: Verwerk meerdere voorwaarden

## Overzicht
De `case`-opdracht in Bash is een krachtige manier om meerdere voorwaarden te evalueren. Het stelt gebruikers in staat om verschillende patronen te vergelijken en op basis daarvan acties uit te voeren. Dit is vooral handig voor het verwerken van invoer of het uitvoeren van verschillende commando's afhankelijk van de waarde van een variabele.

## Gebruik
De basis syntaxis van de `case`-opdracht is als volgt:

```bash
case [variabele] in
    patroon1)
        # acties voor patroon1
        ;;
    patroon2)
        # acties voor patroon2
        ;;
    *)
        # acties voor andere gevallen
        ;;
esac
```

## Veelvoorkomende opties
- `*)`: Dit is een wildcard die overeenkomt met elk patroon dat niet eerder is gedefinieerd. Het wordt vaak gebruikt als een "catch-all" voor onvoorziene waarden.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Eenvoudige case-structuur
```bash
#!/bin/bash
read -p "Voer een getal in (1-3): " getal
case $getal in
    1)
        echo "Je hebt 1 gekozen."
        ;;
    2)
        echo "Je hebt 2 gekozen."
        ;;
    3)
        echo "Je hebt 3 gekozen."
        ;;
    *)
        echo "Ongeldig getal."
        ;;
esac
```

### Voorbeeld 2: Bestandsuitbreiding controleren
```bash
#!/bin/bash
bestand="document.txt"
case $bestand in
    *.txt)
        echo "Dit is een tekstbestand."
        ;;
    *.jpg)
        echo "Dit is een afbeeldingsbestand."
        ;;
    *)
        echo "Onbekend bestandstype."
        ;;
esac
```

### Voorbeeld 3: Maandnamen
```bash
#!/bin/bash
maand=4
case $maand in
    1)
        echo "Januari"
        ;;
    2)
        echo "Februari"
        ;;
    3)
        echo "Maart"
        ;;
    4)
        echo "April"
        ;;
    *)
        echo "Ongeldige maand."
        ;;
esac
```

## Tips
- Gebruik duidelijke en beschrijvende patronen om de leesbaarheid van je script te verbeteren.
- Zorg ervoor dat je de wildcard (`*`) aan het einde van je case-structuur plaatst om onvoorziene waarden af te handelen.
- Test je scripts met verschillende invoerwaarden om ervoor te zorgen dat alle gevallen correct worden afgehandeld.