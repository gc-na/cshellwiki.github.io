# [Linux] Bash head gebruik: Toont de eerste regels van een bestand

## Overzicht
De `head`-opdracht in Bash wordt gebruikt om de eerste regels van een bestand weer te geven. Standaard toont het de eerste 10 regels, maar dit kan worden aangepast met opties.

## Gebruik
De basis syntaxis van de `head`-opdracht is als volgt:

```bash
head [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n [aantal]`: Specificeert het aantal regels dat moet worden weergegeven. Bijvoorbeeld `-n 5` toont de eerste 5 regels.
- `-c [aantal]`: Toont het opgegeven aantal bytes in plaats van regels.
- `-q`: Vermijdt het weergeven van de bestandsnaam bij meerdere bestanden.
- `-v`: Toont altijd de bestandsnaam, zelfs als er maar één bestand is.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `head`-opdracht:

1. Toon de eerste 10 regels van een bestand:
   ```bash
   head bestand.txt
   ```

2. Toon de eerste 5 regels van een bestand:
   ```bash
   head -n 5 bestand.txt
   ```

3. Toon de eerste 20 bytes van een bestand:
   ```bash
   head -c 20 bestand.txt
   ```

4. Toon de eerste 10 regels van meerdere bestanden:
   ```bash
   head bestand1.txt bestand2.txt
   ```

5. Toon de eerste 10 regels van een bestand zonder de bestandsnaam:
   ```bash
   head -q bestand1.txt bestand2.txt
   ```

## Tips
- Gebruik `head` in combinatie met andere commando's, zoals `grep`, om snel de eerste regels van gefilterde resultaten te bekijken.
- Combineer `head` met `tail` om specifieke secties van een bestand te bekijken.
- Vergeet niet dat je met de `-n` optie ook negatieve waarden kunt gebruiken om regels van onderaf te tonen, bijvoorbeeld `head -n -5 bestand.txt` toont alle regels behalve de laatste 5.