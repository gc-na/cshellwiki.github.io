# [Linux] Bash tr gebruik: Tekst transformatie en filtering

## Overzicht
De `tr` (translate) opdracht in Bash wordt gebruikt om tekens in tekstbestanden te vertalen of te verwijderen. Het is een krachtige tool voor het manipuleren van tekststromen, vaak gebruikt in combinatie met andere commando's in de commandoregel.

## Gebruik
De basis syntaxis van de `tr` opdracht is als volgt:

```bash
tr [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d`: Verwijdert de opgegeven tekens uit de invoer.
- `-s`: Vervangt opeenvolgende herhalingen van een teken door één exemplaar.
- `-c`: Specificeert complementaire tekens, d.w.z. alle tekens behalve de opgegeven.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Verander kleine letters naar hoofdletters
```bash
echo "hallo wereld" | tr 'a-z' 'A-Z'
```
Dit commando verandert alle kleine letters in hoofdletters, resulterend in "HALLO WERELD".

### Voorbeeld 2: Verwijder cijfers uit een tekst
```bash
echo "123abc456" | tr -d '0-9'
```
Hiermee worden alle cijfers uit de invoer verwijderd, wat resulteert in "abc".

### Voorbeeld 3: Vervang spaties door nieuwe regels
```bash
echo "regel één regel twee" | tr ' ' '\n'
```
Dit commando vervangt elke spatie door een nieuwe regel, waardoor de uitvoer als volgt is:
```
regel
één
regel
twee
```

### Voorbeeld 4: Samengestelde spaties reduceren
```bash
echo "Dit    is    een    test" | tr -s ' '
```
Hiermee worden opeenvolgende spaties samengevoegd tot één enkele spatie, wat resulteert in "Dit is een test".

## Tips
- Combineer `tr` met andere commando's zoals `grep` of `awk` voor geavanceerdere tekstverwerking.
- Gebruik `echo` of `cat` om tekst naar `tr` te sturen voor eenvoudige transformaties.
- Test je commando's met kleine tekstfragmenten voordat je ze op grotere bestanden toepast om onbedoelde wijzigingen te voorkomen.