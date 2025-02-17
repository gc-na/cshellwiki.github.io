# [Linux] Bash printf gebruik: Formatteren van uitvoer

## Overzicht
De `printf`-opdracht in Bash wordt gebruikt om geformatteerde uitvoer naar de standaarduitvoer te sturen. Het biedt meer controle over de opmaak van de uitvoer dan de standaard `echo`-opdracht, waardoor het ideaal is voor het weergeven van gegevens in een specifieke indeling.

## Gebruik
De basis syntaxis van de `printf`-opdracht is als volgt:

```bash
printf [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties voor `printf`:

- `-v VAR`: Slaat de uitvoer op in de variabele VAR in plaats van deze naar de standaarduitvoer te sturen.
- `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `--version`: Toont de versie-informatie van de `printf`-opdracht.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Eenvoudige tekstuitvoer
```bash
printf "Hallo, wereld!\n"
```
Dit geeft de tekst "Hallo, wereld!" weer, gevolgd door een nieuwe regel.

### Voorbeeld 2: Geformatteerde getallen
```bash
printf "Het getal is: %.2f\n" 3.14159
```
Dit toont "Het getal is: 3.14", waarbij het getal op twee decimalen is afgerond.

### Voorbeeld 3: Meerdere argumenten
```bash
printf "Naam: %s, Leeftijd: %d\n" "Jan" 30
```
Dit geeft "Naam: Jan, Leeftijd: 30" weer, waarbij `%s` staat voor een string en `%d` voor een geheel getal.

### Voorbeeld 4: Opslaan in een variabele
```bash
printf -v resultaat "De som is: %d" $((5 + 3))
echo "$resultaat"
```
Dit slaat de geformatteerde tekst op in de variabele `resultaat` en toont deze vervolgens.

## Tips
- Gebruik `\n` om nieuwe regels toe te voegen in je uitvoer.
- Experimenteer met verschillende formatteringsopties zoals `%s` voor strings, `%d` voor gehele getallen en `%.2f` voor decimale getallen.
- Houd rekening met de volgorde van argumenten in je formatteerstring; deze moeten overeenkomen met de volgorde van de opgegeven waarden.