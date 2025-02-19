# [Linux] C Shell (csh) mkdir gebruik: Mappen maken

## Overzicht
De `mkdir` (make directory) opdracht in C Shell (csh) wordt gebruikt om nieuwe mappen (directories) aan te maken in het bestandssysteem.

## Gebruik
De basis syntaxis van de `mkdir` opdracht is als volgt:

```csh
mkdir [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-p`: Maak ook alle tussenliggende mappen aan als ze nog niet bestaan.
- `-m`: Stel de permissies in voor de nieuwe map (bijvoorbeeld `-m 755`).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mkdir` opdracht:

1. Maak een enkele map aan:
   ```csh
   mkdir nieuwe_map
   ```

2. Maak meerdere mappen tegelijk aan:
   ```csh
   mkdir map1 map2 map3
   ```

3. Maak een map aan met specifieke permissies:
   ```csh
   mkdir -m 700 beveiligde_map
   ```

4. Maak een map aan met tussenliggende mappen:
   ```csh
   mkdir -p pad/naar/nieuwe_map
   ```

## Tips
- Gebruik de `-p` optie om te voorkomen dat je fouten krijgt als tussenliggende mappen niet bestaan.
- Controleer altijd de permissies van de nieuwe map met de `ls -l` opdracht om ervoor te zorgen dat ze correct zijn ingesteld.
- Geef duidelijke en beschrijvende namen aan je mappen om de organisatie van je bestanden te verbeteren.