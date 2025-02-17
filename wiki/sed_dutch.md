# [Linux] Bash sed gebruik: tekstverwerking en -manipulatie

## Overzicht
De `sed` (stream editor) opdracht is een krachtige tool voor tekstverwerking in de Bash-omgeving. Het stelt gebruikers in staat om tekstbestanden te bewerken, te transformeren en te manipuleren via een reeks opdrachten en scripts.

## Gebruik
De basis syntaxis van de `sed` opdracht is als volgt:

```bash
sed [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-e`: Voegt een script toe aan de opdrachten die uitgevoerd moeten worden.
- `-i`: Wijzigt het bestand in plaats van de uitvoer naar de standaarduitvoer te sturen.
- `-n`: Schakelt de standaard uitvoer uit; alleen expliciet aangegeven uitvoer wordt getoond.
- `s/patroon/vervanging/`: Vervangt het patroon met de vervanging in de tekst.

## Veelvoorkomende Voorbeelden

### 1. Basis vervanging
Vervang het woord "oud" door "nieuw" in een tekstbestand.

```bash
sed 's/oud/nieuw/' bestand.txt
```

### 2. Vervangen in het bestand zelf
Gebruik de `-i` optie om de wijziging direct in het bestand door te voeren.

```bash
sed -i 's/oud/nieuw/' bestand.txt
```

### 3. Meerdere vervangingen
Voer meerdere vervangingen uit in één opdracht.

```bash
sed -e 's/oud/nieuw/' -e 's/voorbeeld/test/' bestand.txt
```

### 4. Verwijderen van lege regels
Verwijder lege regels uit een bestand.

```bash
sed '/^$/d' bestand.txt
```

### 5. Specifieke regel vervangen
Vervang alleen de tekst op regel 3.

```bash
sed '3s/oud/nieuw/' bestand.txt
```

## Tips
- Gebruik de `-n` optie samen met `p` om alleen specifieke regels te tonen die aan een patroon voldoen.
- Maak gebruik van backslashes (`\`) om speciale tekens in patronen te ontsnappen.
- Test je `sed` opdrachten met een kopie van je bestand om onbedoelde wijzigingen te voorkomen.