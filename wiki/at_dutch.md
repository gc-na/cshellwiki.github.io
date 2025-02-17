# [Linux] Bash bij at: Tijdgebonden taken plannen

## Overzicht
De `at`-opdracht in Bash wordt gebruikt om taken op een specifieke tijd in de toekomst uit te voeren. Dit is handig voor het plannen van eenmalige opdrachten die op een later tijdstip moeten worden uitgevoerd, zonder dat je een continue achtergrondproces hoeft te draaien.

## Gebruik
De basis syntaxis van de `at`-opdracht is als volgt:

```bash
at [opties] [tijd]
```

Hierbij geef je de tijd op waarop je de opdracht wilt laten uitvoeren.

## Veelvoorkomende opties
- `-f <bestand>`: Voer de opdrachten uit die in het opgegeven bestand staan.
- `-m`: Stuur een e-mail naar de gebruiker als de taak is uitgevoerd, zelfs als er geen uitvoer is.
- `-q <wachtrij>`: Specificeer een wachtrij voor de taak. Standaard is dit 'a'.
- `-V`: Toon de versie van de `at`-opdracht.

## Veelvoorkomende voorbeelden

### Een eenvoudige taak plannen
Plan een opdracht om een script uit te voeren om 15:00 uur:

```bash
echo "bash /pad/naar/script.sh" | at 15:00
```

### Een taak plannen met een specifieke datum
Plan een opdracht om een bestand op 1 januari om 10:00 uur te kopiëren:

```bash
echo "cp /pad/naar/oorspronkelijk_bestand /pad/naar/doel_bestand" | at 10:00 01-01-2024
```

### Een taak plannen vanuit een bestand
Als je meerdere opdrachten hebt, kun je deze in een bestand plaatsen en het bestand uitvoeren:

```bash
at -f /pad/naar/opdrachten.txt 16:00
```

### Een taak plannen met e-mailnotificatie
Plan een opdracht en ontvang een e-mail na uitvoering:

```bash
echo "echo 'Taak uitgevoerd'" | at -m 20:00
```

## Tips
- Zorg ervoor dat de `atd`-dienst actief is op je systeem, anders worden geplande taken niet uitgevoerd.
- Gebruik de `atq`-opdracht om een lijst van geplande taken te bekijken.
- Met de `atrm`-opdracht kun je een geplande taak annuleren door het taaknummer op te geven.