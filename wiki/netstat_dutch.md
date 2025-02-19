# [Linux] C Shell (csh) netstat gebruik: Toont netwerkverbindingen en -statistieken

## Overzicht
Het `netstat`-commando is een netwerkhulpmiddel dat informatie geeft over netwerkverbindingen, routingtabellen, interface-statistieken en meer. Het is nuttig voor het monitoren van netwerkactiviteit en het oplossen van netwerkproblemen.

## Gebruik
De basis syntaxis van het `netstat`-commando is als volgt:

```csh
netstat [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`: Toont alle verbindingen en luisterende poorten.
- `-n`: Toont netwerkadressen en poorten in numerieke vorm in plaats van de hostnamen.
- `-r`: Toont de routingtabel.
- `-i`: Toont informatie over netwerkinterfaces.
- `-s`: Toont statistieken per protocol.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van het `netstat`-commando:

1. **Toon alle actieve verbindingen:**
   ```csh
   netstat -a
   ```

2. **Toon alleen luisterende poorten:**
   ```csh
   netstat -an | grep LISTEN
   ```

3. **Toon de routingtabel:**
   ```csh
   netstat -r
   ```

4. **Toon statistieken per protocol:**
   ```csh
   netstat -s
   ```

5. **Toon informatie over netwerkinterfaces:**
   ```csh
   netstat -i
   ```

## Tips
- Gebruik de optie `-n` om de uitvoer te versnellen door hostnamen te vermijden.
- Combineer opties voor meer gedetailleerde informatie, bijvoorbeeld `netstat -anr` om zowel actieve verbindingen als de routingtabel te zien.
- Controleer regelmatig de netwerkstatistieken om ongebruikelijke activiteit te detecteren.