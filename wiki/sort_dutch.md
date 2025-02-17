# [Linux] Bash sort gebruik: Sorteer tekstbestanden of invoer

## Overzicht
De `sort`-opdracht in Bash wordt gebruikt om de regels van een tekstbestand of invoer te sorteren. Het kan gegevens sorteren op basis van verschillende criteria, zoals alfabetisch of numeriek, en biedt verschillende opties om de sortering aan te passen.

## Gebruik
De basis syntaxis van de `sort`-opdracht is als volgt:

```bash
sort [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n`: Sorteer numeriek in plaats van alfabetisch.
- `-r`: Sorteer in omgekeerde volgorde.
- `-k`: Specificeer de kolom waarop gesorteerd moet worden.
- `-u`: Verwijder dubbele regels in de uitvoer.
- `-o`: Schrijf de gesorteerde uitvoer naar een bestand.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `sort`-opdracht:

1. **Basis sorteren van een bestand:**
   ```bash
   sort bestand.txt
   ```

2. **Numeriek sorteren van een bestand:**
   ```bash
   sort -n cijfers.txt
   ```

3. **Omgekeerd sorteren:**
   ```bash
   sort -r namen.txt
   ```

4. **Sorteren op een specifieke kolom:**
   ```bash
   sort -k 2 gegevens.txt
   ```

5. **Dubbele regels verwijderen en sorteren:**
   ```bash
   sort -u lijst.txt
   ```

6. **Sorteren en uitvoer naar een bestand schrijven:**
   ```bash
   sort -o gesorteerd.txt bestand.txt
   ```

## Tips
- Gebruik de optie `-n` als je met getallen werkt om ervoor te zorgen dat ze correct worden gesorteerd.
- Combineer opties om de sortering aan te passen aan je behoeften, bijvoorbeeld `sort -n -r` voor omgekeerd numeriek sorteren.
- Vergeet niet dat `sort` standaard de invoer alfabetisch sorteert, dus controleer je gegevens voordat je de opdracht uitvoert.