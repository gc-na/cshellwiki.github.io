# [Linux] C Shell (csh) screen gebruik: Beheer van meerdere terminalsessies

## Overzicht
De `screen`-opdracht is een krachtige tool die gebruikers in staat stelt om meerdere terminalsessies binnen één enkele terminalvenster te beheren. Het stelt je in staat om sessies te splitsen, te detacheren en later weer aan te sluiten, wat vooral handig is voor langdurige processen of wanneer je verbinding maakt met een server.

## Gebruik
De basis syntaxis van de `screen`-opdracht is als volgt:

```bash
screen [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-S naam`: Geef een naam aan de nieuwe sessie.
- `-d -r`: Detach een sessie en sluit deze opnieuw aan.
- `-list`: Toon een lijst van actieve sessies.
- `-L`: Schakel logging in voor de sessie.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `screen`:

1. **Een nieuwe sessie starten:**
   ```bash
   screen
   ```

2. **Een nieuwe sessie met een specifieke naam starten:**
   ```bash
   screen -S mijn_sessie
   ```

3. **Detacheren van een sessie:**
   Druk op `Ctrl-a` gevolgd door `d`.

4. **Lijst van actieve sessies bekijken:**
   ```bash
   screen -list
   ```

5. **Een bestaande sessie opnieuw aansluiten:**
   ```bash
   screen -r mijn_sessie
   ```

6. **Detacheren en opnieuw aansluiten in één stap:**
   ```bash
   screen -d -r mijn_sessie
   ```

## Tips
- Gebruik een duidelijke naam voor je sessies, zodat je ze gemakkelijk kunt identificeren.
- Maak gebruik van de loggingfunctie (`-L`) om een geschiedenis van je sessie op te slaan.
- Vergeet niet dat je met `Ctrl-a` gevolgd door `?` een lijst van sneltoetsen kunt bekijken voor extra functionaliteit.