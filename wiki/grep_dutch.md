# [Linux] C Shell (csh) grep gebruik: Zoek naar tekst in bestanden

## Overzicht
De `grep`-opdracht is een krachtige tool die wordt gebruikt om tekstpatronen te zoeken in bestanden. Het kan worden gebruikt om specifieke regels te vinden die overeenkomen met een opgegeven patroon, wat het een onmisbaar hulpmiddel maakt voor programmeurs en systeembeheerders.

## Gebruik
De basis syntaxis van de `grep`-opdracht is als volgt:

```csh
grep [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i`: Negeer hoofdlettergebruik bij het zoeken.
- `-v`: Toon alleen de regels die **niet** overeenkomen met het patroon.
- `-r`: Zoek recursief in alle bestanden in een directory.
- `-n`: Toon het regelnummer van elke overeenkomst.
- `-l`: Toon alleen de namen van bestanden met overeenkomsten.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `grep`:

1. Zoek naar een specifiek woord in een bestand:
   ```csh
   grep "woord" bestand.txt
   ```

2. Zoek naar een woord zonder rekening te houden met hoofdletters:
   ```csh
   grep -i "woord" bestand.txt
   ```

3. Zoek naar een woord in alle tekstbestanden in een directory:
   ```csh
   grep "woord" *.txt
   ```

4. Zoek recursief naar een patroon in een directory:
   ```csh
   grep -r "woord" /pad/naar/directory
   ```

5. Toon de regelnummer van overeenkomsten:
   ```csh
   grep -n "woord" bestand.txt
   ```

## Tips
- Gebruik de `-v` optie om snel te filteren op ongewenste resultaten.
- Combineer `grep` met andere commando's zoals `ls` of `cat` door gebruik te maken van pijpen (`|`) om de uitvoer van het ene commando door te geven aan `grep`.
- Maak gebruik van reguliere expressies voor complexere zoekopdrachten, zoals het zoeken naar patronen in plaats van specifieke woorden.