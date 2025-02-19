# [Linux] C Shell (csh) iconv gebruik: Tekstcodering converteren

## Overzicht
De `iconv`-opdracht wordt gebruikt om tekstbestanden van de ene tekencodering naar de andere te converteren. Dit is nuttig wanneer je bestanden hebt die in verschillende coderingen zijn opgeslagen en je ze wilt uniformeren of compatibel maken met andere systemen.

## Gebruik
De basis syntaxis van de `iconv`-opdracht is als volgt:

```csh
iconv [opties] [argumenten]
```

## Veelvoorkomende opties
- `-f`, `--from-code`: Specificeert de broncodering van de invoer.
- `-t`, `--to-code`: Specificeert de doelcodering voor de uitvoer.
- `-o`, `--output`: Geeft de naam van het uitvoerbestand op.
- `-l`, `--list`: Lijst alle ondersteunde coderingen.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basis conversie
Converteer een bestand van ISO-8859-1 naar UTF-8.

```csh
iconv -f ISO-8859-1 -t UTF-8 input.txt -o output.txt
```

### Voorbeeld 2: Lijst van ondersteunde coderingen
Bekijk de lijst van alle ondersteunde coderingen.

```csh
iconv -l
```

### Voorbeeld 3: Directe uitvoer naar de terminal
Converteer een bestand en toon de uitvoer direct in de terminal.

```csh
iconv -f UTF-16 -t UTF-8 input.txt
```

### Voorbeeld 4: Converteer en overschrijf het originele bestand
Converteer een bestand en overschrijf het originele bestand met de nieuwe codering.

```csh
iconv -f ISO-8859-1 -t UTF-8 input.txt > temp.txt && mv temp.txt input.txt
```

## Tips
- Controleer altijd de bron- en doelcoderingen voordat je een conversie uitvoert om gegevensverlies te voorkomen.
- Maak een back-up van je bestanden voordat je ze converteert, vooral als je ze gaat overschrijven.
- Gebruik de `-l` optie om te verifiëren of de gewenste coderingen worden ondersteund door jouw versie van `iconv`.