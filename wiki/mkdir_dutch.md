# [Linux] Bash mkdir gebruik: Mappen maken

## Overzicht
De `mkdir` (make directory) opdracht in Bash wordt gebruikt om nieuwe mappen (of directories) aan te maken in het bestandssysteem. Het is een fundamentele opdracht die vaak wordt gebruikt bij het organiseren van bestanden en mappen.

## Gebruik
De basis syntaxis van de `mkdir` opdracht is als volgt:

```bash
mkdir [opties] [argumenten]
```

## Veelvoorkomende opties
- `-p`: Maak ook de bovenliggende mappen aan indien deze nog niet bestaan.
- `-v`: Toon een bericht voor elke gemaakte map.
- `-m`: Stel de permissies in voor de nieuwe map.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mkdir` opdracht:

1. **Een enkele map maken:**
   ```bash
   mkdir nieuwe_map
   ```

2. **Meerdere mappen tegelijk maken:**
   ```bash
   mkdir map1 map2 map3
   ```

3. **Een map maken met bovenliggende mappen:**
   ```bash
   mkdir -p /pad/naar/nieuwe/map
   ```

4. **Een map maken en de permissies instellen:**
   ```bash
   mkdir -m 755 nieuwe_map
   ```

5. **Een map maken met een bevestigingsbericht:**
   ```bash
   mkdir -v nieuwe_map
   ```

## Tips
- Gebruik de `-p` optie om te voorkomen dat je fouten krijgt als je probeert een map te maken in een niet-bestaande hiërarchie.
- Controleer altijd of de map al bestaat voordat je `mkdir` gebruikt om onnodige foutmeldingen te vermijden.
- Combineer `mkdir` met andere opdrachten zoals `cd` om efficiënt te navigeren en nieuwe mappen te maken in je workflow.