# [Linux] Bash getopts gebruik: Verwerken van commandoregelopties

## Overzicht
De `getopts`-opdracht in Bash wordt gebruikt om commandoregelopties te parseren. Het stelt scripts in staat om invoerparameters te verwerken op een gestructureerde manier, waardoor gebruikers hun scripts flexibeler kunnen maken.

## Gebruik
De basis syntaxis van de `getopts`-opdracht is als volgt:

```bash
getopts "opties" variabele
```

Hierbij worden de "opties" gedefinieerd als een string van toegestane opties, en de "variabele" is de naam van de variabele waarin de huidige optie wordt opgeslagen.

## Veelvoorkomende Opties
- `-a`: Een voorbeeldoptie die kan worden gebruikt om een bepaalde actie uit te voeren.
- `-b`: Een andere voorbeeldoptie die een alternatieve functie kan activeren.
- `-c`: Vaak gebruikt voor het inschakelen van een configuratie-instelling.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Basisgebruik van getopts
In dit voorbeeld wordt `getopts` gebruikt om een enkele optie te verwerken:

```bash
#!/bin/bash

while getopts "a:" opt; do
  case $opt in
    a)
      echo "Optie -a met waarde: $OPTARG"
      ;;
    \?)
      echo "Ongeldige optie: -$OPTARG" >&2
      ;;
  esac
done
```

### Voorbeeld 2: Meerdere opties
Hier is een voorbeeld dat meerdere opties verwerkt:

```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Optie -a geactiveerd"
      ;;
    b)
      echo "Optie -b met waarde: $OPTARG"
      ;;
    c)
      echo "Optie -c met waarde: $OPTARG"
      ;;
    \?)
      echo "Ongeldige optie: -$OPTARG" >&2
      ;;
  esac
done
```

### Voorbeeld 3: Standaardwaarde instellen
In dit voorbeeld wordt een standaardwaarde ingesteld als er geen optie wordt opgegeven:

```bash
#!/bin/bash

value="standaard"

while getopts "a:b:" opt; do
  case $opt in
    a)
      value=$OPTARG
      ;;
    b)
      value=$OPTARG
      ;;
    \?)
      echo "Ongeldige optie: -$OPTARG" >&2
      ;;
  esac
done

echo "Waarde is: $value"
```

## Tips
- Gebruik altijd een `case`-structuur om de opties te verwerken, dit maakt je script overzichtelijker.
- Vergeet niet om een standaardactie te definiëren voor ongeldige opties om gebruikersfeedback te geven.
- Test je scripts met verschillende combinaties van opties om ervoor te zorgen dat ze correct functioneren.