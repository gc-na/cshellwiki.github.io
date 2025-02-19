# [Linux] C Shell (csh) mv gebruik: Verplaatsen of hernoemen van bestanden

## Overzicht
De `mv`-opdracht in C Shell (csh) wordt gebruikt om bestanden of mappen te verplaatsen of te hernoemen. Het is een essentiële tool voor bestandbeheer in de commandoregelomgeving.

## Gebruik
De basis syntaxis van de `mv`-opdracht is als volgt:

```
mv [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i`: Vraagt om bevestiging voordat een bestaand bestand wordt overschreven.
- `-u`: Verplaatst alleen als de bron nieuwer is dan de bestemming of als de bestemming niet bestaat.
- `-v`: Geeft gedetailleerde informatie over de uitgevoerde acties.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mv`-opdracht:

1. **Een bestand verplaatsen naar een andere map:**
   ```csh
   mv bestand.txt /pad/naar/doelmap/
   ```

2. **Een bestand hernoemen:**
   ```csh
   mv oud_bestand.txt nieuw_bestand.txt
   ```

3. **Meerdere bestanden verplaatsen naar een andere map:**
   ```csh
   mv bestand1.txt bestand2.txt /pad/naar/doelmap/
   ```

4. **Een bestand verplaatsen met bevestiging bij overschrijven:**
   ```csh
   mv -i bestand.txt /pad/naar/doelmap/
   ```

5. **Een bestand verplaatsen als het nieuwer is:**
   ```csh
   mv -u bestand.txt /pad/naar/doelmap/
   ```

## Tips
- Gebruik de `-i` optie om te voorkomen dat je per ongeluk belangrijke bestanden overschrijft.
- Controleer altijd de bestemming voordat je bestanden verplaatst om te voorkomen dat je ze kwijt raakt.
- Maak gebruik van de `-v` optie om te zien wat er gebeurt tijdens het verplaatsen, vooral wanneer je met meerdere bestanden werkt.