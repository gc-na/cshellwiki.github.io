# [Linux] Bash w gebruik: toon ingelogde gebruikers en hun activiteiten

## Overzicht
De `w`-opdracht in Bash toont informatie over de gebruikers die momenteel zijn ingelogd op het systeem, evenals hun actieve processen. Het biedt een overzicht van wie er is ingelogd, hun activiteit en hoe lang ze al zijn ingelogd.

## Gebruik
De basis syntaxis van de `w`-opdracht is als volgt:

```bash
w [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties voor de `w`-opdracht:

- `-h`: Verberg de header van de uitvoer.
- `-s`: Toon een kortere uitvoer zonder extra informatie.
- `-f`: Toon het volledige pad van de terminal.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `w`-opdracht:

1. Gewone uitvoer van ingelogde gebruikers:
    ```bash
    w
    ```

2. Uitvoer zonder header:
    ```bash
    w -h
    ```

3. Korte uitvoer:
    ```bash
    w -s
    ```

4. Uitvoer met volledige terminalpaden:
    ```bash
    w -f
    ```

## Tips
- Gebruik `w` regelmatig om te controleren wie er op het systeem is ingelogd en wat ze aan het doen zijn.
- Combineer `w` met andere commando's zoals `grep` om specifieke gebruikers of activiteiten te filteren.
- Houd rekening met de privacy van andere gebruikers; gebruik `w` op een respectvolle manier.