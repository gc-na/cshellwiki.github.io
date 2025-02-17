# [Linux] Bash bg gebruik: Voer een taak op de achtergrond uit

## Overzicht
De `bg`-opdracht in Bash wordt gebruikt om een taak die momenteel op de achtergrond draait, opnieuw op de achtergrond te plaatsen. Dit is handig wanneer je een proces wilt laten doorgaan terwijl je verder werkt in de terminal.

## Gebruik
De basis syntaxis van de `bg`-opdracht is als volgt:

```bash
bg [opties] [argumenten]
```

## Veelvoorkomende opties
- `job_spec`: Dit is de specificatie van de taak die je wilt hervatten. Dit kan een jobnummer zijn of een jobnaam.
- `-n`: Hiermee wordt de job op de achtergrond uitgevoerd zonder dat deze automatisch naar de standaard uitvoer wordt gestuurd.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Een taak op de achtergrond plaatsen
Stel dat je een lange taak hebt gestart, zoals een bestand kopiëren, en je wilt deze op de achtergrond plaatsen:

```bash
cp grote_bestand.txt /backup/ &
bg
```

### Voorbeeld 2: Een specifieke taak opnieuw op de achtergrond plaatsen
Als je een taak hebt gepauzeerd met `Ctrl+Z`, kun je deze opnieuw op de achtergrond plaatsen met:

```bash
bg %1
```
Hierbij is `%1` het jobnummer van de taak die je wilt hervatten.

### Voorbeeld 3: Meerdere taken op de achtergrond beheren
Je kunt meerdere taken op de achtergrond hebben en ze beheren met hun jobnummers:

```bash
jobs  # Lijst alle taken op
bg %2  # Plaats de tweede taak op de achtergrond
```

## Tips
- Gebruik de `jobs`-opdracht om een lijst van actieve taken te bekijken voordat je `bg` gebruikt.
- Vergeet niet dat je ook `fg` kunt gebruiken om een taak weer naar de voorgrond te brengen als dat nodig is.
- Het is een goede gewoonte om lange taken op de achtergrond te plaatsen, zodat je de terminal voor andere opdrachten kunt blijven gebruiken.