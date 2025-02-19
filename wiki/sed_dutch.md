# [Linux] C Shell (csh) sed Gebruik: tekstverwerking en -transformatie

## Overzicht
De `sed` (stream editor) opdracht is een krachtige tool voor tekstverwerking in de C Shell. Het stelt gebruikers in staat om tekstbestanden te bewerken, te transformeren en te manipuleren op basis van specifieke patronen en instructies.

## Gebruik
De basis syntaxis van de `sed` opdracht is als volgt:

```bash
sed [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-e`: Hiermee kan je meerdere bewerkingen in één opdracht uitvoeren.
- `-i`: Wijzig het bestand in plaats van de uitvoer naar de standaarduitvoer te sturen.
- `-n`: Schakel de standaard uitvoer uit, zodat alleen expliciet opgegeven regels worden weergegeven.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Vervangen van tekst
Vervang alle voorkomens van "oud" met "nieuw" in een bestand genaamd `bestand.txt`.

```bash
sed 's/oud/nieuw/g' bestand.txt
```

### Voorbeeld 2: Regels verwijderen
Verwijder alle lege regels uit een bestand.

```bash
sed '/^$/d' bestand.txt
```

### Voorbeeld 3: In-place bewerking
Vervang "fout" met "correct" en sla de wijzigingen direct op in `bestand.txt`.

```bash
sed -i 's/fout/correct/g' bestand.txt
```

### Voorbeeld 4: Meerdere bewerkingen
Voer meerdere vervangingen uit in één opdracht.

```bash
sed -e 's/oud/nieuw/g' -e 's/fout/correct/g' bestand.txt
```

## Tips
- Test je `sed` opdrachten eerst zonder de `-i` optie om te voorkomen dat je per ongeluk bestanden wijzigt.
- Gebruik aanhalingstekens om je `sed` commando's te omringen, vooral als je variabelen of speciale tekens gebruikt.
- Maak gebruik van reguliere expressies voor meer geavanceerde patroonherkenning en -vervanging.