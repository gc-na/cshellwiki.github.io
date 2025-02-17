# [Linux] Bash lvs gebruik: Toon logische volumenaam informatie

## Overzicht
De `lvs` opdracht in Bash wordt gebruikt om informatie weer te geven over logische volumes in een Logical Volume Manager (LVM) systeem. Het biedt een overzicht van de logische volumes, inclusief hun grootte, status en andere relevante details.

## Gebruik
De basis syntaxis van de `lvs` opdracht is als volgt:

```bash
lvs [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a` : Toon ook verborgen volumes.
- `-o` : Specificeer welke kolommen moeten worden weergegeven.
- `-n` : Geef de naam van het logische volume op.
- `--units` : Specificeer de eenheden voor de uitvoer (bijv. k, M, G).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `lvs` opdracht:

1. **Toon alle logische volumes:**
   ```bash
   lvs
   ```

2. **Toon verborgen logische volumes:**
   ```bash
   lvs -a
   ```

3. **Toon specifieke kolommen (bijv. naam en grootte):**
   ```bash
   lvs -o lv_name,lv_size
   ```

4. **Toon informatie over een specifiek logische volume:**
   ```bash
   lvs -n mijn_volume
   ```

5. **Toon logische volumes met een specifieke eenheid:**
   ```bash
   lvs --units g
   ```

## Tips
- Gebruik de `-o` optie om alleen de informatie te tonen die je nodig hebt, wat de uitvoer overzichtelijker maakt.
- Combineer `lvs` met andere LVM-opdrachten zoals `vgs` en `pvs` voor een completer overzicht van je opslagstructuur.
- Controleer regelmatig je logische volumes om ervoor te zorgen dat ze goed functioneren en voldoende ruimte hebben.