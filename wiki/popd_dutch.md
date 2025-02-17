# [Linux] Bash popd gebruik: Verander naar de vorige directory

## Overzicht
De `popd` opdracht wordt gebruikt om de bovenste directory van de directorystack te verwijderen en terug te keren naar de vorige directory. Dit is handig voor het navigeren tussen verschillende directories zonder het volledige pad opnieuw te hoeven typen.

## Gebruik
De basis syntaxis van de `popd` opdracht is als volgt:

```bash
popd [options]
```

## Veelvoorkomende opties
- `-n`: Voorkomt het wijzigen van de huidige directory, maar verwijdert de directory van de stack.
- `+n`: Verwijdert de directory op de n-de positie van de stack in plaats van de bovenste.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Terugkeren naar de vorige directory
```bash
cd /pad/naar/eerste/directory
pushd /pad/naar/tweede/directory
popd
```
In dit voorbeeld ga je eerst naar de eerste directory, dan naar de tweede met `pushd`, en met `popd` keer je terug naar de eerste directory.

### Voorbeeld 2: Gebruik van de `-n` optie
```bash
pushd /pad/naar/eerste/directory
pushd /pad/naar/tweede/directory
popd -n
```
Hier wordt de tweede directory verwijderd van de stack, maar je blijft in de tweede directory.

### Voorbeeld 3: Terugkeren naar een specifieke directory in de stack
```bash
pushd /pad/naar/eerste/directory
pushd /pad/naar/tweede/directory
pushd /pad/naar/derde/directory
popd +1
```
In dit geval verwijder je de derde directory en keer je terug naar de tweede directory.

## Tips
- Gebruik `dirs` om de huidige status van de directorystack te bekijken.
- Combineer `pushd` en `popd` om efficiënt te navigeren tussen meerdere directories.
- Wees voorzichtig met de `+n` optie, omdat het kan leiden tot verwarring als je niet goed oplet welke directory je verwijdert.