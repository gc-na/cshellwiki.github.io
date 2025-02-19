# [Linux] C Shell (csh) pidstat gebruik: Monitoren van processtatistieken

## Overzicht
Het `pidstat` commando is een handig hulpmiddel voor het monitoren van de prestaties van processen op een systeem. Het biedt gedetailleerde informatie over CPU-gebruik, geheugenverbruik en andere statistieken per proces, wat nuttig is voor systeembeheerders en ontwikkelaars om de prestaties van hun applicaties te analyseren.

## Gebruik
De basis syntaxis van het `pidstat` commando is als volgt:

```csh
pidstat [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties voor `pidstat`:

- `-h`: Toon de resultaten in een leesbaar formaat met eenheden.
- `-r`: Toon informatie over het geheugenverbruik van processen.
- `-u`: Toon CPU-gebruik per proces.
- `-p <PID>`: Specificeer de PID van het proces dat je wilt monitoren.
- `-t`: Toon informatie over threads van processen.

## Veelvoorkomende Voorbeelden

Hier zijn enkele praktische voorbeelden van het gebruik van `pidstat`:

1. **Basis CPU-gebruik per proces tonen**:
   ```csh
   pidstat -u
   ```

2. **Geheugenverbruik van processen weergeven**:
   ```csh
   pidstat -r
   ```

3. **Specifieke PID monitoren**:
   ```csh
   pidstat -p 1234
   ```

4. **CPU- en geheugenstatistieken in een leesbaar formaat tonen**:
   ```csh
   pidstat -h -u -r
   ```

5. **Statistieken voor alle threads van een proces weergeven**:
   ```csh
   pidstat -t -p 1234
   ```

## Tips
- Gebruik de `-h` optie voor een betere leesbaarheid van de output.
- Combineer opties om meer gedetailleerde informatie te krijgen, zoals CPU- en geheugenstatistieken tegelijk.
- Monitor processen regelmatig om trends in prestaties te identificeren en problemen vroegtijdig op te sporen.