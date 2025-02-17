# [Linux] Bash ps gebruik: Toon actieve processen

## Overzicht
De `ps` (process status) opdracht in Bash wordt gebruikt om informatie weer te geven over actieve processen op een Linux-systeem. Het biedt een momentopname van de huidige processen, inclusief details zoals proces-ID, status en gebruik van systeembronnen.

## Gebruik
De basis syntaxis van de `ps` opdracht is als volgt:

```bash
ps [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties die je kunt gebruiken met de `ps` opdracht:

- `-e` of `-A`: Toon alle processen.
- `-f`: Toon uitgebreide informatie over processen.
- `-u [gebruikersnaam]`: Toon processen die door een specifieke gebruiker worden uitgevoerd.
- `-p [PID]`: Toon informatie over een specifiek proces met een gegeven proces-ID.
- `--sort`: Sorteer de uitvoer op basis van een opgegeven veld.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `ps` opdracht:

1. Toon alle actieve processen:
   ```bash
   ps -e
   ```

2. Toon processen met uitgebreide informatie:
   ```bash
   ps -ef
   ```

3. Toon processen van een specifieke gebruiker:
   ```bash
   ps -u username
   ```

4. Toon informatie over een specifiek proces:
   ```bash
   ps -p 1234
   ```

5. Sorteer processen op gebruik van CPU:
   ```bash
   ps -eo pid,comm,%cpu --sort=-%cpu
   ```

## Tips
- Gebruik `ps aux` voor een gedetailleerd overzicht van alle processen, inclusief die van andere gebruikers.
- Combineer `ps` met `grep` om specifieke processen te filteren. Bijvoorbeeld:
  ```bash
  ps -ef | grep firefox
  ```
- Vergeet niet dat de uitvoer van `ps` een momentopname is; processen kunnen snel starten of stoppen, dus voer de opdracht opnieuw uit voor actuele informatie.