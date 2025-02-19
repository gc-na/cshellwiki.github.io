# [Linux] C Shell (csh) head gebruik: weergave van het begin van bestanden

## Overzicht
De `head`-opdracht in C Shell (csh) wordt gebruikt om de eerste regels van een of meerdere bestanden weer te geven. Dit is handig om snel een overzicht te krijgen van de inhoud van een bestand zonder het volledig te openen.

## Gebruik
De basis syntaxis van de `head`-opdracht is als volgt:

```csh
head [opties] [argumenten]
```

## Veelvoorkomende opties
- `-n [aantal]`: Geef het opgegeven aantal regels weer in plaats van de standaard 10 regels.
- `-q`: Weergave van de bestandsnamen onderdrukken wanneer meerdere bestanden worden opgegeven.
- `-v`: Weergave van de bestandsnamen altijd weergeven, zelfs als er maar één bestand is.

## Veelvoorkomende voorbeelden

1. Toon de eerste 10 regels van een bestand:
   ```csh
   head bestand.txt
   ```

2. Toon de eerste 5 regels van een bestand:
   ```csh
   head -n 5 bestand.txt
   ```

3. Toon de eerste 10 regels van meerdere bestanden:
   ```csh
   head bestand1.txt bestand2.txt
   ```

4. Toon de eerste 3 regels van een bestand zonder de bestandsnaam weer te geven:
   ```csh
   head -q -n 3 bestand.txt
   ```

5. Toon de eerste 15 regels van een bestand en geef altijd de bestandsnaam weer:
   ```csh
   head -v -n 15 bestand.txt
   ```

## Tips
- Gebruik `head` in combinatie met andere commando's, zoals `grep`, om snel de eerste regels van gefilterde resultaten te bekijken.
- Combineer `head` met `less` voor een paginagrote weergave van de eerste regels.
- Vergeet niet dat `head` standaard de eerste 10 regels weergeeft; pas dit aan met de `-n` optie indien nodig.