# [Linux] Bash script gebruik: Voer een shell-sessie op en sla deze op

## Overzicht
De `script`-opdracht in Bash wordt gebruikt om een shell-sessie op te nemen en deze op te slaan in een bestand. Dit is handig voor het documenteren van een sessie of het delen van de uitvoer met anderen.

## Gebruik
De basis syntaxis van de `script`-opdracht is als volgt:

```bash
script [opties] [bestandsnaam]
```

## Veelvoorkomende opties
- `-a`: Voeg de uitvoer toe aan een bestaand bestand in plaats van het te overschrijven.
- `-q`: Voer de opdracht uit in stille modus, zonder meldingen te tonen.
- `-t`: Maak een timing-bestand aan dat de tijdstippen van de uitvoer vastlegt.

## Veelvoorkomende voorbeelden

1. **Een nieuwe sessie opnemen in een bestand**:
   ```bash
   script sessie.txt
   ```
   Dit start een nieuwe shell-sessie en slaat alle uitvoer op in `sessie.txt`.

2. **Een sessie opnemen en toevoegen aan een bestaand bestand**:
   ```bash
   script -a sessie.txt
   ```
   Dit voegt de uitvoer van de nieuwe sessie toe aan `sessie.txt` zonder de bestaande inhoud te overschrijven.

3. **Een sessie opnemen in stille modus**:
   ```bash
   script -q sessie.txt
   ```
   Dit start een sessie en slaat de uitvoer op in `sessie.txt`, zonder meldingen weer te geven.

4. **Een sessie opnemen met timing-informatie**:
   ```bash
   script -t 2> timing.txt sessie.txt
   ```
   Dit maakt een opname van de sessie en slaat de timing-informatie op in `timing.txt`.

## Tips
- Gebruik de `-a` optie als je meerdere sessies wilt combineren in één bestand.
- Controleer de inhoud van het opgenomen bestand met `cat` of `less` om ervoor te zorgen dat alles correct is vastgelegd.
- Vergeet niet om de sessie te beëindigen door `exit` of `Ctrl+D` in te voeren, zodat het bestand correct wordt opgeslagen.