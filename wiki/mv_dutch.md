# [Linux] Bash mv gebruik: Verplaatsen of hernoemen van bestanden

## Overzicht
De `mv`-opdracht in Bash wordt gebruikt om bestanden en mappen te verplaatsen of te hernoemen. Het is een essentiële tool voor bestandsbeheer in een Linux-omgeving.

## Gebruik
De basis syntaxis van de `mv`-opdracht is als volgt:

```bash
mv [opties] [bronnen] [doel]
```

## Veelvoorkomende opties
- `-i`: Vraagt om bevestiging voordat een bestaand bestand wordt overschreven.
- `-u`: Verplaatst alleen als de bron nieuwer is dan de bestemming of als de bestemming niet bestaat.
- `-v`: Geeft gedetailleerde informatie over wat er gebeurt tijdens het verplaatsen of hernoemen van bestanden.

## Veelvoorkomende voorbeelden
1. **Een bestand verplaatsen naar een andere map:**
   ```bash
   mv bestand.txt /pad/naar/doelmap/
   ```

2. **Een bestand hernoemen:**
   ```bash
   mv oud_bestand.txt nieuw_bestand.txt
   ```

3. **Meerdere bestanden verplaatsen naar een andere map:**
   ```bash
   mv bestand1.txt bestand2.txt /pad/naar/doelmap/
   ```

4. **Een bestand verplaatsen met bevestiging:**
   ```bash
   mv -i bestand.txt /pad/naar/doelmap/
   ```

5. **Een bestand verplaatsen als het nieuwer is dan het doelbestand:**
   ```bash
   mv -u bestand.txt /pad/naar/doelmap/
   ```

## Tips
- Gebruik de `-i` optie om onbedoeld overschrijven van bestanden te voorkomen.
- Controleer altijd de bestandslocaties voordat je bestanden verplaatst of hernoemt om verwarring te voorkomen.
- Maak gebruik van de `-v` optie om een beter inzicht te krijgen in de uitgevoerde acties, vooral wanneer je met meerdere bestanden werkt.