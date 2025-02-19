# [Linux] C Shell (csh) killall gebruik: Proces beëindigen op basis van naam

## Overzicht
De `killall`-opdracht in C Shell (csh) wordt gebruikt om processen te beëindigen op basis van hun naam. Dit is handig wanneer je meerdere instanties van een programma wilt afsluiten zonder ze één voor één te hoeven zoeken.

## Gebruik
De basis syntaxis van de `killall`-opdracht is als volgt:

```csh
killall [opties] [argumenten]
```

## Veelvoorkomende opties
- `-u <gebruiker>`: Beëindig alleen de processen die door de opgegeven gebruiker worden uitgevoerd.
- `-9`: Dwingt het beëindigen van processen, zelfs als ze niet reageren op normale beëindigingssignalen.
- `-r`: Gebruik reguliere expressies om processen te matchen.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `killall`:

1. Beëindig alle processen met de naam `gedit`:
   ```csh
   killall gedit
   ```

2. Beëindig alle processen met de naam `firefox` met een dwingend signaal:
   ```csh
   killall -9 firefox
   ```

3. Beëindig processen die door een specifieke gebruiker worden uitgevoerd:
   ```csh
   killall -u gebruikernaam
   ```

4. Gebruik een reguliere expressie om processen te beëindigen die beginnen met `python`:
   ```csh
   killall -r python.*
   ```

## Tips
- Wees voorzichtig met het gebruik van `-9`, omdat dit processen kan beëindigen zonder ze de kans te geven om hun werk op te slaan.
- Controleer altijd welke processen je gaat beëindigen, vooral als je als root werkt, om onbedoelde gevolgen te voorkomen.
- Gebruik `ps` of `pgrep` om de processen te controleren voordat je `killall` uitvoert, zodat je zeker weet dat je de juiste processen beëindigt.