# [Linux] Bash top gebruik: Bekijk systeemprocessen in real-time

## Overzicht
De `top`-opdracht is een krachtige tool in Linux die een dynamisch overzicht biedt van de actieve processen op het systeem. Het toont informatie zoals CPU- en geheugengebruik, waardoor gebruikers snel inzicht krijgen in de prestaties van hun systeem.

## Gebruik
De basis syntaxis van de `top`-opdracht is als volgt:

```bash
top [opties]
```

## Veelvoorkomende opties
Hier zijn enkele veelvoorkomende opties die je kunt gebruiken met de `top`-opdracht:

- `-d <tijd>`: Stel de update-interval in (in seconden).
- `-p <pid>`: Toon alleen processen met de opgegeven proces-ID.
- `-u <gebruikersnaam>`: Toon alleen processen die door de opgegeven gebruiker worden uitgevoerd.

## Veelvoorkomende voorbeelden

1. **Basis gebruik van top**:
   ```bash
   top
   ```

2. **Top met een update-interval van 2 seconden**:
   ```bash
   top -d 2
   ```

3. **Top voor een specifieke gebruiker**:
   ```bash
   top -u gebruiker
   ```

4. **Top voor een specifieke proces-ID**:
   ```bash
   top -p 1234
   ```

## Tips
- Druk op `h` binnen de `top`-interface voor een helpmenu met sneltoetsen.
- Gebruik `Shift + M` om processen te sorteren op geheugengebruik.
- Druk op `q` om de `top`-interface te verlaten.