# [Linux] Bash rsync gebruik: Bestanden synchroniseren en overdragen

## Overzicht
De `rsync`-opdracht is een krachtige tool voor het synchroniseren en overdragen van bestanden en mappen tussen verschillende locaties, zowel lokaal als op afstand. Het biedt efficiëntie door alleen de wijzigingen in bestanden over te dragen, wat tijd en bandbreedte bespaart.

## Gebruik
De basis syntaxis van de `rsync`-opdracht is als volgt:

```bash
rsync [opties] [bronnen] [doel]
```

## Veelvoorkomende opties
- `-a`: Archiveer modus; kopieert bestanden en mappen recursief en behoudt bestandspermissies, tijdstempels, enz.
- `-v`: Verbose; toont gedetailleerde uitvoer van het proces.
- `-z`: Comprimeert de gegevens tijdens de overdracht voor snellere transfers.
- `-r`: Recursief; kopieert mappen en hun inhoud.
- `--delete`: Verwijdert bestanden in de doelmap die niet in de brondirectory staan.
- `-e`: Specificeert het gebruik van een andere shell, zoals SSH, voor veilige overdracht.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `rsync`:

1. **Basisbestanden kopiëren:**
   ```bash
   rsync -av /pad/naar/bronnen/ /pad/naar/doel/
   ```

2. **Bestanden synchroniseren met compressie:**
   ```bash
   rsync -avz /pad/naar/bronnen/ gebruiker@server:/pad/naar/doel/
   ```

3. **Bestanden synchroniseren en verwijderen van oude bestanden:**
   ```bash
   rsync -av --delete /pad/naar/bronnen/ /pad/naar/doel/
   ```

4. **Gebruik van SSH voor veilige overdracht:**
   ```bash
   rsync -av -e ssh /pad/naar/bronnen/ gebruiker@server:/pad/naar/doel/
   ```

## Tips
- Gebruik de `-n` of `--dry-run` optie om te zien welke acties `rsync` zou ondernemen zonder daadwerkelijk bestanden te kopiëren of te verwijderen.
- Zorg ervoor dat je de juiste paden opgeeft om onbedoeld gegevensverlies te voorkomen, vooral bij het gebruik van de `--delete` optie.
- Overweeg het gebruik van een cronjob om regelmatig synchronisaties uit te voeren voor back-updoeleinden.