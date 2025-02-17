# [Linux] Bash dirname gebruik: Bepaal de directory van een pad

## Overzicht
De `dirname` opdracht in Bash wordt gebruikt om het pad van de directory te extraheren uit een volledig pad naar een bestand of een map. Het retourneert de directory-naam zonder de bestandsnaam.

## Gebruik
De basis syntaxis van de `dirname` opdracht is als volgt:

```bash
dirname [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-z`: Behandel lege invoer als een lege string.
- `--help`: Toon een helpbericht met informatie over het gebruik van de opdracht.
- `--version`: Toon de versie-informatie van de `dirname` opdracht.

## Veelvoorkomende Voorbeelden

1. **Basisgebruik**:
   Om de directory van een bestandspad te verkrijgen:
   ```bash
   dirname /home/gebruiker/documenten/bestand.txt
   ```
   **Output**:
   ```
   /home/gebruiker/documenten
   ```

2. **Gebruik met een relatieve pad**:
   Voor een relatieve pad kan de opdracht ook worden gebruikt:
   ```bash
   dirname documenten/bestand.txt
   ```
   **Output**:
   ```
   documenten
   ```

3. **Meerdere paden**:
   Je kunt meerdere paden tegelijk opgeven:
   ```bash
   dirname /home/gebruiker/documenten/bestand.txt /var/log/syslog
   ```
   **Output**:
   ```
   /home/gebruiker/documenten
   /var/log
   ```

4. **Met een lege invoer**:
   Bij een lege invoer retourneert `dirname` een lege regel:
   ```bash
   dirname ""
   ```
   **Output**:
   ```
   (lege regel)
   ```

## Tips
- Gebruik `dirname` in scripts om dynamisch de directory van bestanden te verkrijgen, wat handig is voor bestandsbeheer.
- Combineer `dirname` met andere opdrachten zoals `find` of `xargs` voor geavanceerdere bestandsoperaties.
- Vergeet niet dat `dirname` alleen de directory retourneert en geen bestandsinformatie, dus gebruik het in combinatie met andere opdrachten voor volledige functionaliteit.