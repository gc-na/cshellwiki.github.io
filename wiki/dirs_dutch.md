# [Linux] Bash dirs gebruik: Beheer van de directory stack

## Overzicht
De `dirs` opdracht in Bash wordt gebruikt om de inhoud van de directory stack weer te geven. Deze stack houdt een lijst bij van de directories die je hebt bezocht met de `pushd` en `popd` commando's. Het is een handige manier om snel tussen verschillende directories te navigeren.

## Gebruik
De basis syntaxis van de `dirs` opdracht is als volgt:

```bash
dirs [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l`: Toont de directories in een lange lijstvorm.
- `-p`: Toont de directories in een padvorm, wat nuttig kan zijn voor een snellere weergave.

## Veelvoorkomende Voorbeelden

1. **Toon de huidige directory stack:**
   ```bash
   dirs
   ```

2. **Toon de directory stack in lange lijstvorm:**
   ```bash
   dirs -l
   ```

3. **Toon de directory stack in padvorm:**
   ```bash
   dirs -p
   ```

4. **Gebruik `pushd` en `popd` om directories toe te voegen en te verwijderen:**
   ```bash
   pushd /pad/naar/directory
   dirs
   popd
   dirs
   ```

## Tips
- Gebruik `pushd` en `popd` samen met `dirs` om efficiënt te navigeren tussen verschillende directories.
- Vergeet niet dat de volgorde van de directories in de stack belangrijk is; de bovenste directory is de huidige werkdirectory.
- Experimenteer met de opties om te zien welke weergave het beste voor jou werkt.