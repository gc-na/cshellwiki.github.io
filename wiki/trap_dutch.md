# [Linux] C Shell (csh) trap gebruik: Beheer signalen en beëindigingen

## Overzicht
De `trap`-opdracht in C Shell (csh) wordt gebruikt om signalen en beëindigingen van processen te beheren. Hiermee kun je specifieke acties definiëren die moeten worden uitgevoerd wanneer een bepaald signaal wordt ontvangen, zoals het beëindigen van een script of het uitvoeren van een opruimactie.

## Gebruik
De basis syntaxis van de `trap`-opdracht is als volgt:

```csh
trap [actie] [signaal]
```

## Veelvoorkomende opties
- `action`: De actie die moet worden uitgevoerd wanneer het opgegeven signaal wordt ontvangen. Dit kan een commando zijn of een reeks commando's.
- `signal`: Het signaal dat je wilt opvangen, zoals `INT` (interrupt), `TERM` (terminate) of `QUIT`.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basis gebruik van trap
Dit voorbeeld toont hoe je een script kunt beëindigen met een bericht wanneer het `INT`-signaal (bijvoorbeeld Ctrl+C) wordt ontvangen.

```csh
#!/bin/csh
trap 'echo "Script beëindigd door gebruiker"; exit' INT
while (1)
    echo "Script draait..."
    sleep 1
end
```

### Voorbeeld 2: Opruimactie bij beëindiging
Hier is een voorbeeld waarbij een opruimactie wordt uitgevoerd voordat het script wordt beëindigd.

```csh
#!/bin/csh
trap 'echo "Opruimen..."; rm -f temp.txt; exit' TERM
echo "Script draait. Stuur een TERM signaal om te beëindigen."
while (1)
    sleep 1
end
```

### Voorbeeld 3: Meerdere signalen opvangen
In dit voorbeeld worden meerdere signalen opgevangen en wordt dezelfde actie uitgevoerd.

```csh
#!/bin/csh
trap 'echo "Script beëindigd"; exit' INT TERM
while (1)
    echo "Script draait..."
    sleep 1
end
```

## Tips
- Zorg ervoor dat je de juiste signalen opvangt die relevant zijn voor jouw script.
- Gebruik duidelijke en informatieve berichten in je acties om de gebruiker te informeren over wat er gebeurt.
- Test je scripts grondig om ervoor te zorgen dat de `trap`-opdrachten correct functioneren in verschillende scenario's.