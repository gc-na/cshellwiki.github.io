# [Linux] C Shell (csh) rsync gebruik: Bestanden synchroniseren

## Overzicht
De `rsync`-opdracht is een krachtige tool voor het synchroniseren van bestanden en mappen tussen verschillende locaties. Het wordt vaak gebruikt voor back-ups en het overbrengen van bestanden over netwerken, omdat het alleen de gewijzigde delen van bestanden overzet, wat tijd en bandbreedte bespaart.

## Gebruik
De basis syntaxis van de `rsync`-opdracht is als volgt:

```csh
rsync [opties] [bronnen] [doel]
```

## Veelvoorkomende Opties
- `-a`: Archiveer modus; kopieert bestanden en mappen recursief en behoudt de meeste bestandsattributen.
- `-v`: Verbose; toont gedetailleerde informatie tijdens de uitvoering.
- `-z`: Comprimeert de gegevens tijdens de overdracht om bandbreedte te besparen.
- `-r`: Recursief; kopieert mappen en hun inhoud.
- `--delete`: Verwijdert bestanden in de doelmap die niet in de bronomgeving aanwezig zijn.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `rsync`:

1. **Basis synchronisatie van een lokale map naar een andere lokale map:**
   ```csh
   rsync -av /pad/naar/bronnen/ /pad/naar/doel/
   ```

2. **Synchroniseren van een lokale map naar een externe server:**
   ```csh
   rsync -av /pad/naar/bronnen/ gebruiker@server:/pad/naar/doel/
   ```

3. **Synchroniseren met compressie om bandbreedte te besparen:**
   ```csh
   rsync -avz /pad/naar/bronnen/ gebruiker@server:/pad/naar/doel/
   ```

4. **Synchroniseren en verwijderen van bestanden die niet meer bestaan in de bronomgeving:**
   ```csh
   rsync -av --delete /pad/naar/bronnen/ /pad/naar/doel/
   ```

## Tips
- Gebruik de `-n` of `--dry-run` optie om te zien welke bestanden zouden worden gekopieerd zonder daadwerkelijk iets te veranderen.
- Zorg ervoor dat je de juiste paden opgeeft om onbedoeld verlies van gegevens te voorkomen.
- Overweeg het gebruik van SSH voor veilige overdracht van bestanden naar externe servers door `rsync` te combineren met SSH.