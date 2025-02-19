# [Linux] C Shell (csh) watch gebruik: Voortdurend een commando uitvoeren

## Overzicht
De `watch` opdracht in C Shell (csh) stelt gebruikers in staat om een specifiek commando op regelmatige tijdstippen uit te voeren en de uitvoer in real-time te bekijken. Dit is bijzonder nuttig voor het monitoren van veranderingen in de uitvoer van een commando, zoals systeemstatistieken of logbestanden.

## Gebruik
De basis syntaxis van de `watch` opdracht is als volgt:

```csh
watch [opties] [argumenten]
```

## Veelvoorkomende opties
- `-n <seconden>`: Bepaalt de intervaltijd in seconden tussen de uitvoeringen van het commando. Standaard is dit 2 seconden.
- `-d`: Markeer de wijzigingen in de uitvoer door de gewijzigde regels te benadrukken.
- `-t`: Verberg de header die de tijd en het commando toont.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Systeemprocessen monitoren
Voer het `ps` commando uit elke 5 seconden om actieve processen te bekijken:
```csh
watch -n 5 ps aux
```

### Voorbeeld 2: Schijfruimte controleren
Controleer de schijfruimte op de schijven elke 10 seconden:
```csh
watch -n 10 df -h
```

### Voorbeeld 3: Logbestanden volgen
Volg een logbestand en markeer wijzigingen:
```csh
watch -d tail -n 10 /var/log/syslog
```

### Voorbeeld 4: Netwerkverbindingen controleren
Bekijk actieve netwerkverbindingen elke 3 seconden:
```csh
watch -n 3 netstat -tuln
```

## Tips
- Gebruik de `-d` optie om snel veranderingen op te merken in de uitvoer, vooral bij lange lijsten.
- Pas de intervaltijd aan met de `-n` optie om de belasting op het systeem te minimaliseren, vooral bij zware commando's.
- Combineer `watch` met andere commando's om specifieke informatie te monitoren die voor jou belangrijk is.