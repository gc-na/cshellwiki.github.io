# [Linux] Bash @ gebruik: [verander de bestandsnaam]

## Overzicht
De `mv` (move) opdracht in Bash wordt gebruikt om bestanden of mappen te verplaatsen of om de naam van een bestand of map te wijzigen. Het is een veelzijdige opdracht die essentieel is voor bestandsbeheer in een Linux-omgeving.

## Gebruik
De basis syntaxis van de `mv` opdracht is als volgt:

```bash
mv [opties] [bronnen] [doel]
```

## Veelvoorkomende opties
- `-i`: Vraag om bevestiging voordat een bestaand bestand wordt overschreven.
- `-u`: Verplaats alleen als de bron nieuwer is dan de bestemming of als de bestemming niet bestaat.
- `-v`: Toon gedetailleerde uitvoer van wat er gebeurt tijdens de uitvoering van de opdracht.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mv` opdracht:

1. **Bestand verplaatsen naar een andere map:**
   ```bash
   mv bestand.txt /pad/naar/doelmap/
   ```

2. **Bestand hernoemen:**
   ```bash
   mv oude_naam.txt nieuwe_naam.txt
   ```

3. **Meerdere bestanden verplaatsen:**
   ```bash
   mv bestand1.txt bestand2.txt /pad/naar/doelmap/
   ```

4. **Bestand verplaatsen met bevestiging:**
   ```bash
   mv -i bestand.txt /pad/naar/doelmap/
   ```

5. **Bestand verplaatsen met gedetailleerde uitvoer:**
   ```bash
   mv -v bestand.txt /pad/naar/doelmap/
   ```

## Tips
- Gebruik de `-i` optie om per ongeluk overschrijven van bestanden te voorkomen.
- Controleer altijd de bestandslocaties voordat je de `mv` opdracht uitvoert, vooral bij het verplaatsen van belangrijke bestanden.
- Maak gebruik van de `-v` optie om te zien wat er precies gebeurt, vooral als je met meerdere bestanden werkt.