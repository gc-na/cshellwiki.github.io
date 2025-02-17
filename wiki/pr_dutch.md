# [Linux] Bash pr gebruik: Pagina-opmaak voor tekstbestanden

## Overzicht
De `pr` opdracht in Bash wordt gebruikt om tekstbestanden op te maken voor afdrukken. Het verdeelt de inhoud van een bestand in pagina's en kolommen, waardoor het gemakkelijker wordt om te lezen en te printen.

## Gebruik
De basis syntaxis van de `pr` opdracht is als volgt:

```bash
pr [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l [aantal]`: Stel het aantal regels per pagina in.
- `-w [breedte]`: Stel de breedte van de pagina in.
- `-2`: Verdeel de uitvoer in twee kolommen.
- `-t`: Onderdruk de titel en de paginanummers in de uitvoer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `pr` opdracht:

1. **Basis gebruik**: Om een tekstbestand op te maken voor afdrukken.
   ```bash
   pr bestand.txt
   ```

2. **Instellen van het aantal regels per pagina**: Om 50 regels per pagina in te stellen.
   ```bash
   pr -l 50 bestand.txt
   ```

3. **Twee kolommen gebruiken**: Om de uitvoer in twee kolommen te verdelen.
   ```bash
   pr -2 bestand.txt
   ```

4. **Breedte van de pagina instellen**: Om de breedte van de pagina in te stellen op 80 tekens.
   ```bash
   pr -w 80 bestand.txt
   ```

5. **Titel en paginanummers onderdrukken**: Om de titel en paginanummers niet weer te geven.
   ```bash
   pr -t bestand.txt
   ```

## Tips
- Gebruik de optie `-l` om de leesbaarheid te verbeteren, vooral bij lange bestanden.
- Experimenteer met de kolominstellingen om de uitvoer aan te passen aan uw behoeften.
- Combineer opties voor meer geavanceerde opmaak, zoals het instellen van zowel kolommen als pagina breedte.