# [Linux] Bash wc gebruik: Tel het aantal regels, woorden en tekens

## Overzicht
De `wc` (word count) opdracht in Bash wordt gebruikt om het aantal regels, woorden en tekens in een bestand of invoer te tellen. Dit is handig voor het analyseren van tekstbestanden en het verkrijgen van statistieken over de inhoud.

## Gebruik
De basis syntaxis van de `wc` opdracht is als volgt:

```bash
wc [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`: Tel het aantal regels.
- `-w`: Tel het aantal woorden.
- `-c`: Tel het aantal tekens.
- `-m`: Tel het aantal karakters (inclusief multibyte-tekens).
- `-L`: Toon de lengte van de langste regel.

## Veelvoorkomende voorbeelden

1. **Aantal regels in een bestand tellen:**

   ```bash
   wc -l bestand.txt
   ```

2. **Aantal woorden in een bestand tellen:**

   ```bash
   wc -w bestand.txt
   ```

3. **Aantal tekens in een bestand tellen:**

   ```bash
   wc -c bestand.txt
   ```

4. **Aantal regels, woorden en tekens in één keer tellen:**

   ```bash
   wc bestand.txt
   ```

5. **Aantal regels in de standaardinvoer tellen (bijvoorbeeld via echo):**

   ```bash
   echo "Hallo wereld" | wc -l
   ```

## Tips
- Gebruik `wc` in combinatie met andere opdrachten via een pijp (`|`) om snel statistieken van de uitvoer van die opdrachten te verkrijgen.
- Combineer meerdere opties om een uitgebreid overzicht te krijgen, bijvoorbeeld `wc -l -w bestand.txt`.
- Houd rekening met de bestandsindeling; als je werkt met bestanden die verschillende tekencoderingen hebben, kan dit de telling beïnvloeden.