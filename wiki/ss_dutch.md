# [Linux] C Shell (csh) ss gebruik: Netwerkverbindingen weergeven

## Overzicht
De `ss`-opdracht wordt gebruikt om netwerkverbindingen en sockets op een systeem weer te geven. Het is een krachtig hulpmiddel voor het analyseren van netwerkverbindingen en het diagnosticeren van netwerkproblemen.

## Gebruik
De basis syntaxis van de `ss`-opdracht is als volgt:

```csh
ss [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-t`: Toon alleen TCP-sockets.
- `-u`: Toon alleen UDP-sockets.
- `-l`: Toon alleen luisterende sockets.
- `-p`: Toon het proces dat de socket gebruikt.
- `-n`: Toon netwerkadressen en poorten in numerieke vorm.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `ss`-opdracht:

1. **Toon alle actieve verbindingen:**
   ```csh
   ss
   ```

2. **Toon alleen TCP-sockets:**
   ```csh
   ss -t
   ```

3. **Toon alleen luisterende sockets:**
   ```csh
   ss -l
   ```

4. **Toon UDP-sockets met procesinformatie:**
   ```csh
   ss -u -p
   ```

5. **Toon alle verbindingen in numerieke vorm:**
   ```csh
   ss -n
   ```

## Tips
- Gebruik de `-p` optie om te zien welke processen de netwerkverbindingen gebruiken, wat handig kan zijn voor probleemoplossing.
- Combineer opties om gerichte informatie te krijgen, bijvoorbeeld `ss -t -l` om alleen luisterende TCP-sockets te zien.
- Controleer regelmatig de netwerkverbindingen op je systeem om ongewenste of verdachte verbindingen te identificeren.