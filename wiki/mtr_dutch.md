# [Linux] C Shell (csh) mtr gebruik: Netwerkdiagnosetool

## Overzicht
De `mtr` (My Traceroute) opdracht combineert de functionaliteit van `ping` en `traceroute` om netwerkverbindingen te analyseren. Het biedt een dynamisch overzicht van de route die gegevenspakketten nemen naar een specifieke host, samen met informatie over de vertraging en pakketverlies op elke hop.

## Gebruik
De basis syntaxis van de `mtr` opdracht is als volgt:

```csh
mtr [opties] [doel]
```

## Veelvoorkomende Opties
- `-r`: Voer een rapport uit en sluit af.
- `-c [aantal]`: Geef het aantal pings aan dat moet worden verzonden.
- `-i [interval]`: Stel het interval in tussen de pings.
- `-p`: Toon de poortnummers in de uitvoer.
- `-w`: Gebruik een breedte van 80 karakters voor de uitvoer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `mtr`:

1. Basis gebruik om de route naar een host te traceren:
   ```csh
   mtr example.com
   ```

2. Voer een rapport uit met een specifiek aantal pings:
   ```csh
   mtr -r -c 10 example.com
   ```

3. Traceren met een aangepast interval tussen pings:
   ```csh
   mtr -i 2 example.com
   ```

4. Toon de poortnummers in de uitvoer:
   ```csh
   mtr -p example.com
   ```

5. Gebruik een breedte van 80 karakters voor de uitvoer:
   ```csh
   mtr -w example.com
   ```

## Tips
- Gebruik de `-r` optie voor een snelle rapportage als je alleen de resultaten wilt zonder de continue uitvoer.
- Experimenteer met verschillende intervallen en ping-aantallen om een beter beeld te krijgen van netwerkprestaties.
- Combineer `mtr` met andere netwerkdiagnosetools zoals `ping` en `traceroute` voor een grondiger netwerkonderzoek.