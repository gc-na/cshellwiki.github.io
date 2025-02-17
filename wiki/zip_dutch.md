# [Linux] Bash zip gebruik: Bestanden comprimeren

## Overzicht
De `zip`-opdracht is een veelgebruikte tool in de Bash-omgeving voor het comprimeren van bestanden en mappen. Het maakt een gecomprimeerd archiefbestand aan met de extensie `.zip`, waardoor het gemakkelijker wordt om bestanden op te slaan en te delen.

## Gebruik
De basis syntaxis van de `zip`-opdracht is als volgt:

```bash
zip [opties] [archiefnaam] [bestanden]
```

## Veelvoorkomende Opties
- `-r`: Recursief bestanden en mappen toevoegen.
- `-e`: Versleuteling inschakelen voor het archief.
- `-u`: Bestaande bestanden in het archief bijwerken.
- `-d`: Bestanden uit het archief verwijderen.
- `-q`: Stil, geen output tonen tijdens het proces.

## Veelvoorkomende Voorbeelden

1. **Een enkel bestand comprimeren:**
   ```bash
   zip mijn_bestand.zip document.txt
   ```

2. **Meerdere bestanden comprimeren:**
   ```bash
   zip mijn_archief.zip document1.txt document2.txt afbeelding.png
   ```

3. **Een hele map comprimeren:**
   ```bash
   zip -r mijn_map.zip mijn_map/
   ```

4. **Een bestand bijwerken in een bestaand archief:**
   ```bash
   zip -u mijn_archief.zip document.txt
   ```

5. **Een bestand uit een archief verwijderen:**
   ```bash
   zip -d mijn_archief.zip document2.txt
   ```

## Tips
- Gebruik de `-e` optie om gevoelige informatie te beschermen door je archief te versleutelen.
- Controleer altijd de inhoud van je zip-bestand met `unzip -l [archiefnaam]` voordat je het deelt.
- Houd rekening met de bestandsgrootte; grote bestanden kunnen veel tijd kosten om te comprimeren.