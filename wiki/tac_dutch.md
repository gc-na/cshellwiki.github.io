# [Linux] Bash tac Gebruik: Inhoud omkeren

## Overzicht
De `tac` opdracht in Bash wordt gebruikt om de inhoud van een bestand regel voor regel omgekeerd weer te geven. Dit betekent dat de laatste regel van het bestand als eerste wordt weergegeven en de eerste regel als laatste.

## Gebruik
De basis syntaxis van de `tac` opdracht is als volgt:

```bash
tac [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-r`, `--regexp`: Behandelt de invoer als reguliere expressies.
- `-s`, `--separator`: Specificeert een scheidingsteken dat gebruikt wordt om regels te splitsen.
- `-b`, `--before`: Voegt een scheidingsteken toe vóór elke regel in plaats van erna.

## Veelvoorkomende Voorbeelden

1. **Basis gebruik**: Om een bestand omgekeerd weer te geven:
   ```bash
   tac bestand.txt
   ```

2. **Gebruik van een scheidingsteken**: Om een bestand omgekeerd weer te geven met een specifieke scheidingsteken:
   ```bash
   tac -s "," bestand.csv
   ```

3. **Reguliere expressies**: Om een bestand omgekeerd weer te geven met reguliere expressies:
   ```bash
   tac -r bestand.txt
   ```

4. **Omgekeerd weergeven met een scheidingsteken vóór de regels**:
   ```bash
   tac -b -s ";" bestand.txt
   ```

## Tips
- Gebruik `tac` in combinatie met andere commando's via een pijp (`|`) om de uitvoer verder te verwerken.
- Wees voorzichtig met grote bestanden, omdat het omkeren van de inhoud veel geheugen kan vereisen.
- Combineer `tac` met `head` of `tail` om alleen een bepaald aantal omgekeerde regels weer te geven.