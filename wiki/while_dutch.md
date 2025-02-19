# [Linux] C Shell (csh) while gebruiken: Voer herhalende taken uit

## Overzicht
De `while`-opdracht in C Shell (csh) wordt gebruikt om een blok code herhaaldelijk uit te voeren zolang een bepaalde voorwaarde waar is. Dit is handig voor het automatiseren van taken die meerdere keren moeten worden uitgevoerd totdat aan een bepaalde voorwaarde wordt voldaan.

## Gebruik
De basis syntaxis van de `while`-opdracht is als volgt:

```csh
while (voorwaarde)
    commando's
end
```

## Veelvoorkomende Opties
- **voorwaarde**: Een expressie die waar of onwaar kan zijn. De loop blijft draaien zolang deze waar is.
- **commando's**: De opdrachten die herhaaldelijk worden uitgevoerd.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Eenvoudige tel-loop
Dit voorbeeld telt van 1 tot 5.

```csh
set i = 1
while ($i <= 5)
    echo $i
    @ i++
end
```

### Voorbeeld 2: Wacht op een bestand
Dit voorbeeld wacht tot een bestand beschikbaar is.

```csh
set bestand = "mijnbestand.txt"
while (! -e $bestand)
    echo "Wachten op $bestand..."
    sleep 2
end
echo "$bestand is nu beschikbaar."
```

### Voorbeeld 3: Herhaal een commando
Dit voorbeeld herhaalt een commando totdat een bepaalde voorwaarde waar is.

```csh
set getal = 0
while ($getal < 10)
    @ getal += 1
    echo "Huidig getal: $getal"
end
```

## Tips
- Zorg ervoor dat je de voorwaarde correct instelt om oneindige lussen te voorkomen.
- Gebruik `sleep` in je loop om de belasting van de CPU te verminderen als je wacht op een bepaalde gebeurtenis.
- Test je `while`-lussen met een kleine dataset om er zeker van te zijn dat ze correct werken voordat je ze op grotere datasets toepast.