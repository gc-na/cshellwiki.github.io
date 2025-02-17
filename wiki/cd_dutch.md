# [Linux] Bash cd gebruik: Navigeer tussen mappen

## Overview
De `cd` (change directory) opdracht in Bash wordt gebruikt om van de ene map naar de andere te navigeren. Het stelt gebruikers in staat om hun huidige werkdirectory te veranderen, wat essentieel is voor het uitvoeren van verschillende commando's in de juiste context.

## Usage
De basis syntaxis van de `cd` opdracht is als volgt:

```bash
cd [opties] [argumenten]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor de `cd` opdracht:

- `..` : Ga één niveau omhoog in de directorystructuur.
- `-` : Ga terug naar de vorige directory.
- `~` : Ga naar de home directory van de huidige gebruiker.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van de `cd` opdracht:

1. Ga naar een specifieke map:
   ```bash
   cd /pad/naar/map
   ```

2. Ga één niveau omhoog:
   ```bash
   cd ..
   ```

3. Ga terug naar de vorige directory:
   ```bash
   cd -
   ```

4. Ga naar de home directory:
   ```bash
   cd ~
   ```

5. Ga naar een submap binnen de huidige directory:
   ```bash
   cd submapnaam
   ```

## Tips
- Gebruik `pwd` (print working directory) na `cd` om te bevestigen dat je in de juiste directory bent.
- Combineer `cd` met tab-completion om snel door directories te navigeren zonder de volledige naam in te typen.
- Vergeet niet dat de padnamen hoofdlettergevoelig zijn in Linux, dus zorg ervoor dat je de juiste hoofdletters gebruikt.