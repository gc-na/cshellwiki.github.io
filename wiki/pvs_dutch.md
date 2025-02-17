# [Linux] Bash pvs gebruik: Toon informatie over fysieke volumes

## Overzicht
De `pvs` opdracht in Bash wordt gebruikt om informatie weer te geven over fysieke volumes in een Logical Volume Management (LVM) systeem. Het biedt een overzicht van de fysieke opslagapparaten die zijn toegewezen aan de LVM-configuratie.

## Gebruik
De basis syntaxis van de `pvs` opdracht is als volgt:

```bash
pvs [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-o, --options`: Specificeer welke kolommen moeten worden weergegeven.
- `-h, --human-readable`: Toon de uitvoer in een leesbaar formaat (bijvoorbeeld met eenheden zoals GB).
- `-v, --verbose`: Geef meer gedetailleerde informatie weer.
- `--noheadings`: Verberg de koppen in de uitvoer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `pvs` opdracht:

1. **Basisinformatie over fysieke volumes weergeven:**

   ```bash
   pvs
   ```

2. **Informatie in een leesbaar formaat weergeven:**

   ```bash
   pvs -h
   ```

3. **Specifieke kolommen weergeven:**

   ```bash
   pvs -o +pv_size,pv_free
   ```

4. **Gedetailleerde informatie tonen:**

   ```bash
   pvs -v
   ```

5. **Koppen verbergen in de uitvoer:**

   ```bash
   pvs --noheadings
   ```

## Tips
- Gebruik de `-h` optie om de uitvoer gemakkelijker te lezen, vooral bij grote volumes.
- Combineer `pvs` met andere LVM-opdrachten zoals `lvdisplay` en `vgdisplay` voor een completer overzicht van je opslagconfiguratie.
- Controleer regelmatig de status van je fysieke volumes om ervoor te zorgen dat er geen problemen zijn met de opslagcapaciteit.