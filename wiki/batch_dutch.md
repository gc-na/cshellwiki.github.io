# [Linux] C Shell (csh) batch gebruik: Voer taken uit in de achtergrond

## Overzicht
De `batch` opdracht in C Shell (csh) wordt gebruikt om taken in de achtergrond uit te voeren op een later tijdstip. Het is handig voor het plannen van taken die niet onmiddellijk hoeven te worden uitgevoerd, maar die wel op een bepaald moment moeten worden uitgevoerd wanneer de systeembelasting laag is.

## Gebruik
De basis syntaxis van de `batch` opdracht is als volgt:

```
batch [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`: Voer de opdrachten uit met een login shell.
- `-q`: Specificeer een wachtrij voor de batchtaken.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Een eenvoudige batchtaak indienen
Om een eenvoudige opdracht in te dienen die een script uitvoert, gebruik je:

```csh
echo "ls -l" | batch
```

### Voorbeeld 2: Een script indienen
Je kunt ook een script indienen dat je eerder hebt geschreven:

```csh
batch < mijn_script.csh
```

### Voorbeeld 3: Meerdere opdrachten indienen
Je kunt meerdere opdrachten indienen door ze in een enkele echo-opdracht te scheiden met een puntkomma:

```csh
echo "echo 'Taak 1' ; echo 'Taak 2'" | batch
```

## Tips
- Zorg ervoor dat je de juiste rechten hebt om de taken uit te voeren die je indient.
- Controleer regelmatig de status van je batchtaken met de `atq` opdracht.
- Gebruik `atrm` om een batchtaak te annuleren als dat nodig is.