# [Linux] Bash set gebruik: Beheer shell-instellingen en variabelen

## Overzicht
De `set`-opdracht in Bash wordt gebruikt om shell-instellingen en variabelen te beheren. Het stelt gebruikers in staat om bepaalde opties in te schakelen of uit te schakelen, evenals om variabelen in de huidige shell-omgeving te definiëren of te wijzigen.

## Gebruik
De basis syntaxis van de `set`-opdracht is als volgt:

```bash
set [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties voor de `set`-opdracht:

- `-e`: Stop met uitvoeren als een commando een fout retourneert.
- `-u`: Behandel niet-gedefinieerde variabelen als een fout.
- `-x`: Toon de commando's die worden uitgevoerd, handig voor debugging.
- `-o`: Schakel specifieke shell-opties in, zoals `noclobber` of `pipefail`.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Stoppen bij een fout
Gebruik de `-e` optie om de uitvoering te stoppen bij een fout.

```bash
set -e
echo "Dit wordt uitgevoerd"
false
echo "Dit wordt NIET uitgevoerd"
```

### Voorbeeld 2: Debugging met -x
Met de `-x` optie kun je zien welke commando's worden uitgevoerd.

```bash
set -x
echo "Dit is een test"
ls /niet/bestaande/map
set +x
```

### Voorbeeld 3: Niet-gedefinieerde variabelen
Gebruik de `-u` optie om een fout te genereren bij niet-gedefinieerde variabelen.

```bash
set -u
echo $ONBEKENDE_VARIABELE
```

## Tips
- Gebruik `set -e` in scripts om ervoor te zorgen dat je script stopt bij fouten, wat helpt bij het voorkomen van onverwachte resultaten.
- Combineer opties zoals `set -eux` voor een krachtige combinatie van foutafhandeling en debugging.
- Vergeet niet om `set +e` of `set +u` te gebruiken als je de opties wilt uitschakelen voor specifieke delen van je script.