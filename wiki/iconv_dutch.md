# [Linux] Bash iconv gebruik: Conversie van tekstbestanden tussen verschillende coderingen

## Overzicht
De `iconv`-opdracht is een nuttig hulpmiddel in de Bash-omgeving dat wordt gebruikt om tekstbestanden te converteren van de ene karaktercodering naar de andere. Dit is vooral handig bij het werken met bestanden die in verschillende coderingen zijn opgeslagen, zoals UTF-8, ISO-8859-1, en meer.

## Gebruik
De basis syntaxis van de `iconv`-opdracht is als volgt:

```bash
iconv [opties] -f [bron-codering] -t [doel-codering] [bestandsnaam]
```

## Veelvoorkomende opties
- `-f`: Specificeert de broncodering van het bestand.
- `-t`: Specificeert de doelcodering voor de conversie.
- `-o`: Bepaalt de uitvoerbestandsnaam. Als deze optie niet wordt gebruikt, wordt de uitvoer naar de standaarduitvoer gestuurd.
- `-c`: Negeert ongeldige karakters tijdens de conversie.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Conversie van UTF-8 naar ISO-8859-1
```bash
iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
```
In dit voorbeeld wordt het bestand `input.txt`, dat in UTF-8 is gecodeerd, geconverteerd naar ISO-8859-1 en opgeslagen als `output.txt`.

### Voorbeeld 2: Conversie van ISO-8859-1 naar UTF-8
```bash
iconv -f ISO-8859-1 -t UTF-8 input.txt -o output.txt
```
Hier wordt `input.txt`, gecodeerd in ISO-8859-1, geconverteerd naar UTF-8.

### Voorbeeld 3: Conversie met het negeren van ongeldige karakters
```bash
iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
```
In dit geval worden ongeldige karakters genegeerd tijdens de conversie van UTF-8 naar ISO-8859-1.

## Tips
- Controleer altijd de codering van je bestanden voordat je ze converteert. Dit kan je helpen om conversiefouten te voorkomen.
- Gebruik de `-o` optie om de uitvoer naar een nieuw bestand te sturen, zodat je het originele bestand niet overschrijft.
- Test de conversie met een klein bestand om er zeker van te zijn dat de uitvoer naar wens is voordat je grotere bestanden verwerkt.