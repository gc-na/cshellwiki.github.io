# [Linux] Bash exit gebruik: Beëindig een shell-sessie

## Overzicht
De `exit`-opdracht in Bash wordt gebruikt om een shell-sessie te beëindigen. Het kan worden gebruikt in scripts of interactief in de terminal om de huidige shell of het script af te sluiten.

## Gebruik
De basis syntaxis van de `exit`-opdracht is als volgt:

```bash
exit [status]
```

Hierbij is `status` een optioneel argument dat de exitstatus van de shell of het script aangeeft. Een status van 0 geeft aan dat alles goed is verlopen, terwijl een andere waarde een fout aangeeft.

## Veelvoorkomende opties
- `status`: Een geheel getal dat de exitstatus aangeeft. Standaard is dit 0 als er geen argument wordt opgegeven.

## Veelvoorkomende voorbeelden

1. **Eenvoudig afsluiten van de shell**
   ```bash
   exit
   ```

2. **Afsluiten met een specifieke status**
   ```bash
   exit 1
   ```

3. **Afsluiten van een script met een succesvolle status**
   ```bash
   #!/bin/bash
   echo "Script is succesvol uitgevoerd."
   exit 0
   ```

4. **Afsluiten van een subshell**
   ```bash
   (echo "Dit is een subshell"; exit 2)
   echo "Dit is de hoofd shell."
   ```

## Tips
- Gebruik `exit 0` om aan te geven dat een script succesvol is uitgevoerd.
- Gebruik `exit 1` of andere niet-nul waarden om aan te geven dat er een fout is opgetreden.
- Vergeet niet dat als je `exit` in een subshell gebruikt, het alleen die subshell beëindigt en niet de hoofd shell.