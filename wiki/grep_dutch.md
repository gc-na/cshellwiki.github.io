# [Linux] Bash grep gebruik: Zoek tekst in bestanden

## Overzicht
De `grep`-opdracht is een krachtige tool in Bash die wordt gebruikt om tekstpatronen te zoeken in bestanden of standaardinvoer. Het is een essentieel hulpmiddel voor systeembeheerders en ontwikkelaars om snel informatie te vinden.

## Gebruik
De basis syntaxis van de `grep`-opdracht is als volgt:

```bash
grep [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i`: Negeert hoofdletters en kleine letters bij het zoeken.
- `-v`: Toont alleen de regels die **niet** overeenkomen met het patroon.
- `-r`: Doorzoekt bestanden in submappen (recursief).
- `-n`: Geeft het regelnummer weer van de overeenkomende regels.
- `-l`: Toont alleen de namen van bestanden met overeenkomende regels.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `grep`:

1. Zoek naar een specifiek woord in een bestand:
   ```bash
   grep "woord" bestand.txt
   ```

2. Zoek naar een woord zonder rekening te houden met hoofdletters:
   ```bash
   grep -i "woord" bestand.txt
   ```

3. Zoek naar een patroon in alle tekstbestanden in een map:
   ```bash
   grep "patroon" *.txt
   ```

4. Zoek recursief naar een patroon in een map:
   ```bash
   grep -r "patroon" /pad/naar/map
   ```

5. Toon de regelnummer van overeenkomende regels:
   ```bash
   grep -n "woord" bestand.txt
   ```

## Tips
- Gebruik de `-v` optie om snel ongewenste resultaten te filteren.
- Combineer `grep` met andere commando's zoals `ls` of `cat` voor meer geavanceerde zoekopdrachten.
- Maak gebruik van reguliere expressies voor complexere zoekopdrachten.
- Gebruik `grep` in combinatie met `|` (pipe) om de uitvoer van andere commando's te doorzoeken.