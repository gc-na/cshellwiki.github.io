# [Linux] Bash trap gebruik: Beheer signalen en exit-statussen

## Overzicht
De `trap`-opdracht in Bash wordt gebruikt om signalen en exit-statussen te beheren. Hiermee kun je specifieke acties uitvoeren wanneer een script een bepaald signaal ontvangt of wanneer het beëindigd wordt. Dit is handig voor het opschonen van bronnen of het uitvoeren van bepaalde taken voordat een script stopt.

## Gebruik
De basis syntaxis van de `trap`-opdracht is als volgt:

```bash
trap [opties] [commando's]
```

## Veelvoorkomende opties
- `SIGINT`: Dit signaal wordt verzonden wanneer de gebruiker Ctrl+C indrukt. Je kunt `trap` gebruiken om een commando uit te voeren in plaats van het script abrupt te beëindigen.
- `EXIT`: Dit signaal wordt verzonden wanneer het script eindigt. Je kunt hiermee een opruimcommando uitvoeren.
- `SIGTERM`: Dit signaal wordt verzonden om een proces te beëindigen. Je kunt hierop reageren met een specifieke actie.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Afhandelen van SIGINT
Dit voorbeeld toont hoe je een script kunt laten reageren op Ctrl+C:

```bash
trap 'echo "Script onderbroken"; exit' SIGINT
while true; do
    echo "Voer een taak uit..."
    sleep 1
done
```

### Voorbeeld 2: Opruimen bij beëindigen
Hier is een voorbeeld dat een opruimactie uitvoert wanneer het script eindigt:

```bash
trap 'echo "Opruimen..."; rm -f /tmp/mijnbestand' EXIT
echo "Script aan het draaien..."
sleep 5
```

### Voorbeeld 3: Afhandelen van meerdere signalen
In dit voorbeeld worden meerdere signalen afgehandeld:

```bash
trap 'echo "Script beëindigd"; exit' SIGINT SIGTERM
while true; do
    echo "Script draait..."
    sleep 1
done
```

## Tips
- Gebruik `trap` om ervoor te zorgen dat belangrijke opruimacties worden uitgevoerd, zelfs als een script onverwacht wordt beëindigd.
- Test je scripts grondig om er zeker van te zijn dat de `trap`-commando's correct reageren op de gewenste signalen.
- Houd rekening met de volgorde van signalen; sommige signalen kunnen andere signalen overschrijven of negeren.