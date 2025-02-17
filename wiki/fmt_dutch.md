# [Linux] Bash fmt gebruik: Tekst formatteren

## Overzicht
De `fmt`-opdracht is een eenvoudige tekstformatteringshulpmiddel in Bash. Het wordt gebruikt om tekstbestanden te herformatteren, zodat ze een consistente breedte hebben, wat handig is voor het verbeteren van de leesbaarheid.

## Gebruik
De basis syntaxis van de `fmt`-opdracht is als volgt:

```bash
fmt [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-w, --width <nummer>`: Stelt de maximale breedte in voor de regels (standaard is 75 tekens).
- `-s, --split-only`: Splits alleen regels die langer zijn dan de opgegeven breedte, zonder extra spaties toe te voegen.
- `-p, --prefix <prefix>`: Voegt een prefix toe aan elke regel in de uitvoer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `fmt`-opdracht:

1. **Basis formattering van een tekstbestand:**
   ```bash
   fmt tekstbestand.txt
   ```

2. **Formatteren met een specifieke breedte van 50 tekens:**
   ```bash
   fmt -w 50 tekstbestand.txt
   ```

3. **Splits alleen lange regels zonder extra spaties:**
   ```bash
   fmt -s tekstbestand.txt
   ```

4. **Voeg een prefix toe aan elke regel:**
   ```bash
   fmt -p "> " tekstbestand.txt
   ```

## Tips
- Gebruik de `-w` optie om de leesbaarheid van lange teksten te verbeteren, vooral voor documenten die op een terminal worden weergegeven.
- Combineer de `-s` optie met andere opties om meer controle te hebben over hoe de tekst wordt opgemaakt.
- Test de formattering met een klein tekstbestand voordat je het op grotere bestanden toepast, om te zien hoe de uitvoer eruitziet.