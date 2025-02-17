# [Linux] Bash expand gebruik: Tekst met spaties uitbreiden

## Overzicht
Het `expand` commando in Bash wordt gebruikt om tabs in een tekstbestand te vervangen door spaties. Dit is handig voor het uniformiseren van de opmaak van tekstbestanden, vooral wanneer ze worden weergegeven in omgevingen die tabs niet goed ondersteunen.

## Gebruik
De basis syntaxis van het `expand` commando is als volgt:

```bash
expand [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-t, --tabs=TABSTOPS`: Stel de tabstops in op de opgegeven waarden. Standaard is dit 8 spaties.
- `-i, --initial`: Vervang alleen tabs die worden gevolgd door een spatie of een nieuw regel.
- `-n, --no-tabs`: Voorkom dat tabs worden vervangen door spaties.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van het `expand` commando:

1. **Basis gebruik**: Vervang tabs door spaties in een bestand.
   ```bash
   expand bestand.txt
   ```

2. **Tabstops instellen**: Vervang tabs door spaties met aangepaste tabstops.
   ```bash
   expand -t 4 bestand.txt
   ```

3. **Initial tabs vervangen**: Vervang alleen tabs die gevolgd worden door een spatie.
   ```bash
   expand -i bestand.txt
   ```

4. **Resultaat naar een nieuw bestand schrijven**: Sla de output op in een nieuw bestand.
   ```bash
   expand bestand.txt > uitgebreid_bestand.txt
   ```

## Tips
- Gebruik de optie `-t` om de tabstops aan te passen aan de vereisten van je project of omgeving.
- Controleer altijd de output van het `expand` commando door het naar de terminal te sturen voordat je het naar een bestand schrijft, om te zorgen dat de opmaak correct is.
- Combineer `expand` met andere commando's zoals `cat` of `less` voor een betere weergave van bestanden met tabs.