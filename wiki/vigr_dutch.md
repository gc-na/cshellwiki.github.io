# [Linux] Bash vigr gebruik: Bewerken van systeemconfiguratiebestanden

## Overzicht
De `vigr` opdracht is een veilige manier om de `/etc/passwd` en `/etc/group` bestanden te bewerken. Het zorgt ervoor dat de bestanden niet tegelijkertijd door meerdere gebruikers worden gewijzigd, wat kan leiden tot corruptie. `vigr` opent deze bestanden in de standaard teksteditor van de gebruiker, meestal `vi` of `vim`.

## Gebruik
De basis syntaxis van de `vigr` opdracht is als volgt:

```bash
vigr [opties] [bestanden]
```

## Veelvoorkomende Opties
- `-h`, `--help`: Toont een hulpbericht met informatie over het gebruik van de opdracht.
- `-s`, `--safe`: Voorkomt dat de editor wordt geopend als er een probleem is met de bestandsstructuur.
- `-f`, `--file`: Hiermee kunt u een specifiek bestand opgeven om te bewerken in plaats van de standaardbestanden.

## Veelvoorkomende Voorbeelden

1. **Basisgebruik van vigr**:
   Om het `/etc/passwd` bestand te bewerken, gebruik je gewoon:
   ```bash
   vigr
   ```

2. **Bewerken van het `/etc/group` bestand**:
   Om het `/etc/group` bestand te bewerken, kun je het volgende commando gebruiken:
   ```bash
   vigr /etc/group
   ```

3. **Gebruik van de veilige modus**:
   Als je wilt zorgen dat er geen problemen zijn met de bestandsstructuur, gebruik dan de veilige modus:
   ```bash
   vigr -s
   ```

4. **Specifiek bestand bewerken**:
   Om een ander bestand te bewerken, bijvoorbeeld een aangepaste configuratie, gebruik je:
   ```bash
   vigr -f /pad/naar/jouw/bestand
   ```

## Tips
- Zorg ervoor dat je een back-up maakt van belangrijke configuratiebestanden voordat je deze bewerkt.
- Leer de basiscommando's van `vi` of `vim`, aangezien `vigr` deze editors gebruikt.
- Gebruik de veilige modus als je niet zeker bent van de integriteit van het bestand dat je wilt bewerken.