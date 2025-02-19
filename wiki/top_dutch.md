# [Linux] C Shell (csh) top gebruik: Toont actieve processen

## Overzicht
De `top`-opdracht in C Shell (csh) is een krachtige tool die een dynamisch overzicht biedt van de actieve processen op een systeem. Het toont informatie zoals CPU- en geheugengebruik, waardoor gebruikers eenvoudig kunnen zien welke processen veel middelen verbruiken.

## Gebruik
De basis syntaxis van de `top`-opdracht is als volgt:

```
top [opties] [argumenten]
```

## Veelvoorkomende opties
Hier zijn enkele veelvoorkomende opties voor de `top`-opdracht:

- `-d <tijd>`: Stel de verversingssnelheid in (in seconden).
- `-p <PID>`: Toon alleen de processen met de opgegeven proces-ID.
- `-u <gebruikersnaam>`: Toon alleen de processen die aan de opgegeven gebruiker zijn toegewezen.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `top`-opdracht:

1. Start `top` met de standaardinstellingen:
   ```bash
   top
   ```

2. Start `top` met een verversingssnelheid van 5 seconden:
   ```bash
   top -d 5
   ```

3. Toon alleen de processen van een specifieke gebruiker:
   ```bash
   top -u gebruiker
   ```

4. Toon alleen een specifiek proces met een bepaalde PID:
   ```bash
   top -p 1234
   ```

## Tips
- Gebruik de toetsen `h` of `?` binnen `top` voor hulp en meer informatie over de beschikbare sneltoetsen.
- Druk op `q` om `top` te verlaten.
- Experimenteer met de sorteerfuncties door op de kolomkoppen te klikken of de sneltoetsen te gebruiken om processen te sorteren op verschillende criteria, zoals CPU- of geheugengebruik.