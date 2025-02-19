# [Linux] C Shell (csh) stat gebruik: Toont bestandseigenschappen

## Overzicht
De `stat`-opdracht in C Shell (csh) wordt gebruikt om gedetailleerde informatie over bestanden en directories weer te geven. Dit omvat metadata zoals de bestandsgrootte, de laatste wijzigingsdatum en de toegangsrechten.

## Gebruik
De basis syntaxis van de `stat`-opdracht is als volgt:

```csh
stat [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c` : Specificeert een aangepaste uitvoerformaat.
- `-f` : Geeft informatie over het bestandssysteem in plaats van het bestand.
- `-L` : Volgt symbolische links en toont informatie over het doelbestand.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `stat`-opdracht:

1. Basisinformatie over een bestand:
   ```csh
   stat mijnbestand.txt
   ```

2. Informatie over een directory:
   ```csh
   stat /pad/naar/directory
   ```

3. Aangepaste uitvoer met specifieke velden:
   ```csh
   stat -c '%s %y' mijnbestand.txt
   ```

4. Informatie over een symbolische link:
   ```csh
   stat -L mijnlink
   ```

## Tips
- Gebruik de `-c` optie om alleen de informatie te krijgen die je nodig hebt, wat de uitvoer overzichtelijker maakt.
- Combineer `stat` met andere commando's zoals `grep` om specifieke informatie te filteren.
- Controleer altijd de rechten van bestanden met `stat` om ervoor te zorgen dat je de juiste toegang hebt.