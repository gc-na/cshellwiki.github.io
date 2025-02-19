# [Linux] C Shell (csh) diff gebruik: Vergelijk bestanden

## Overzicht
Het `diff`-commando wordt gebruikt om de verschillen tussen twee bestanden of mappen te vergelijken. Het toont de regels die verschillen tussen de twee invoerbestanden, waardoor het een handig hulpmiddel is voor het identificeren van wijzigingen in tekstbestanden.

## Gebruik
De basis syntaxis van het `diff`-commando is als volgt:

```csh
diff [opties] [argumenten]
```

## Veelvoorkomende opties
- `-u`: Toon de verschillen in een uniforme weergave.
- `-c`: Toon de verschillen in een contextweergave.
- `-i`: Negeer hoofdlettergebruik bij het vergelijken.
- `-w`: Negeer witruimtes bij het vergelijken.
- `-r`: Vergelijk mappen recursief.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van het `diff`-commando:

### Voorbeeld 1: Basisvergelijking
Vergelijk twee tekstbestanden en toon de verschillen.
```csh
diff bestand1.txt bestand2.txt
```

### Voorbeeld 2: Uniforme weergave
Gebruik de uniforme optie om de verschillen duidelijker weer te geven.
```csh
diff -u bestand1.txt bestand2.txt
```

### Voorbeeld 3: Contextweergave
Toon de verschillen met context om meer informatie te geven over de wijzigingen.
```csh
diff -c bestand1.txt bestand2.txt
```

### Voorbeeld 4: Vergelijk mappen
Vergelijk twee mappen en hun inhoud recursief.
```csh
diff -r map1/ map2/
```

## Tips
- Gebruik de `-i` optie als je niet wilt dat hoofdletters de vergelijking beïnvloeden.
- Combineer opties voor een meer gedetailleerde output, bijvoorbeeld `diff -u -w bestand1.txt bestand2.txt`.
- Bekijk de man-pagina (`man diff`) voor meer informatie over geavanceerde opties en gebruik.