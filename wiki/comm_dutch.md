# [Linux] C Shell (csh) comm commando: Vergelijk twee gesorteerde bestanden

## Overzicht
Het `comm` commando wordt gebruikt om de overeenkomsten en verschillen tussen twee gesorteerde bestanden te vergelijken. Het toont de regels die uniek zijn voor elk bestand en de regels die in beide bestanden voorkomen.

## Gebruik
De basis syntaxis van het `comm` commando is als volgt:

```csh
comm [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-1`: Onderdruk de uitvoer van regels die alleen in het eerste bestand voorkomen.
- `-2`: Onderdruk de uitvoer van regels die alleen in het tweede bestand voorkomen.
- `-3`: Onderdruk de uitvoer van regels die in beide bestanden voorkomen.
- `-i`: Negeer hoofdlettergebruik bij de vergelijking.

## Veelvoorkomende Voorbeelden

1. **Basisvergelijking van twee bestanden:**
   ```csh
   comm bestand1.txt bestand2.txt
   ```

2. **Alleen tonen van regels die uniek zijn voor het eerste bestand:**
   ```csh
   comm -13 bestand1.txt bestand2.txt
   ```

3. **Tonen van alleen de gemeenschappelijke regels:**
   ```csh
   comm -23 bestand1.txt bestand2.txt
   ```

4. **Vergelijking zonder hoofdlettergevoeligheid:**
   ```csh
   comm -i bestand1.txt bestand2.txt
   ```

## Tips
- Zorg ervoor dat de bestanden gesorteerd zijn voordat je `comm` gebruikt, anders krijg je mogelijk onverwachte resultaten.
- Gebruik de opties om de uitvoer aan te passen aan je behoeften, zodat je alleen de relevante informatie ziet.
- Combineer `comm` met andere commando's zoals `sort` om de efficiëntie te verhogen, bijvoorbeeld: 
  ```csh
  comm <(sort bestand1.txt) <(sort bestand2.txt)
  ```