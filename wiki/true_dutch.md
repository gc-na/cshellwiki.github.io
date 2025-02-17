# [Linux] Bash true gebruik: Voert altijd een succesvolle exitstatus uit

## Overview
De `true` opdracht in Bash is een eenvoudige, maar nuttige commandoregeltool die altijd een succesvolle exitstatus (0) retourneert. Het wordt vaak gebruikt in scripts en commando's waar een succesvolle uitvoering vereist is, maar waar geen specifieke actie nodig is.

## Usage
De basis syntaxis van de `true` opdracht is als volgt:

```bash
true [options] [arguments]
```

## Common Options
De `true` opdracht heeft geen specifieke opties of argumenten. Het is een eenvoudige opdracht die altijd succesvol is.

## Common Examples

### Voorbeeld 1: Basisgebruik
Het eenvoudigste gebruik van `true` is gewoon het uitvoeren van de opdracht:

```bash
true
```

### Voorbeeld 2: Gebruik in een if-structuur
Je kunt `true` gebruiken in een `if`-structuur om altijd de "true" tak te laten uitvoeren:

```bash
if true; then
    echo "Dit zal altijd worden uitgevoerd."
fi
```

### Voorbeeld 3: In een loop
`true` kan ook worden gebruikt in een oneindige loop:

```bash
while true; do
    echo "Dit blijft doorgaan totdat het proces wordt gestopt."
    sleep 1
done
```

### Voorbeeld 4: Als placeholder
Je kunt `true` gebruiken als een placeholder in scripts waar je later een echte opdracht wilt toevoegen:

```bash
# TODO: Voeg hier een echte opdracht toe
true
```

## Tips
- Gebruik `true` als een placeholder in scripts om de structuur te behouden terwijl je aan de functionaliteit werkt.
- Combineer `true` met andere commando's in een pipeline om altijd een succesvolle status te garanderen.
- Wees voorzichtig met het gebruik van `true` in loops, omdat dit kan leiden tot oneindige uitvoeringen als er geen exit-voorwaarde is.