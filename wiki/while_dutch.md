# [Linux] Bash while gebruik: Herhaal een commando zolang een voorwaarde waar is

## Overview
De `while`-lus in Bash is een controle structuur die een bepaalde set commando's herhaaldelijk uitvoert zolang een opgegeven voorwaarde waar is. Dit maakt het een krachtig hulpmiddel voor het automatiseren van taken die herhaald moeten worden totdat aan een bepaalde voorwaarde is voldaan.

## Usage
De basis syntaxis van de `while`-lus is als volgt:

```bash
while [voorwaarde]; do
    # commando's
done
```

## Common Options
De `while`-lus zelf heeft geen specifieke opties, maar de voorwaarde die je gebruikt kan verschillende testcommando's bevatten, zoals:
- `-e`: controleer of een bestand bestaat.
- `-f`: controleer of een bestand een regulier bestand is.
- `-d`: controleer of een bestand een directory is.
- `-z`: controleer of een string leeg is.

## Common Examples

### Voorbeeld 1: Eenvoudige tel lus
Dit voorbeeld telt van 1 tot 5 en print elk nummer.

```bash
count=1
while [ $count -le 5 ]; do
    echo $count
    ((count++))
done
```

### Voorbeeld 2: Wacht tot een bestand beschikbaar is
Dit voorbeeld wacht tot een bestand genaamd `bestand.txt` beschikbaar is.

```bash
while [ ! -e bestand.txt ]; do
    echo "Wachten op bestand..."
    sleep 2
done
echo "Bestand gevonden!"
```

### Voorbeeld 3: Lees lijnen uit een bestand
Dit voorbeeld leest elke lijn uit een bestand en print deze.

```bash
while IFS= read -r line; do
    echo "Lijn: $line"
done < bestand.txt
```

## Tips
- Zorg ervoor dat je de voorwaarde correct instelt om oneindige lussen te voorkomen.
- Gebruik `sleep` in je `while`-lus om de belasting op de CPU te verminderen bij het wachten op een voorwaarde.
- Test je scripts met een kleine dataset voordat je ze op grotere bestanden of in productieomgevingen uitvoert.