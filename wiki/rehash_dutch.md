# [Linux] Bash rehash gebruik: Herlaad de commando-cache

## Overzicht
De `rehash`-opdracht in Bash is een nuttige functie die de interne cache van de shell bijwerkt. Dit is vooral handig wanneer je nieuwe uitvoerbare bestanden hebt toegevoegd aan je pad of wanneer je wijzigingen hebt aangebracht in bestaande uitvoerbare bestanden. Door `rehash` uit te voeren, kan de shell deze nieuwe of gewijzigde bestanden herkennen zonder dat je de terminal opnieuw hoeft op te starten.

## Gebruik
De basis syntaxis van de `rehash`-opdracht is als volgt:

```bash
rehash [opties] [argumenten]
```

## Veelvoorkomende Opties
De `rehash`-opdracht heeft geen specifieke opties, maar het kan nuttig zijn om te weten dat het zonder argumenten wordt uitgevoerd om de cache te vernieuwen.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Gewoon rehashen
Om de commando-cache te vernieuwen, voer je simpelweg het volgende commando in:

```bash
rehash
```

### Voorbeeld 2: Na het installeren van een nieuw programma
Stel dat je een nieuw programma hebt geïnstalleerd en je wilt ervoor zorgen dat het beschikbaar is in je huidige shell-sessie:

```bash
rehash
```

### Voorbeeld 3: Na het wijzigen van een script
Als je een script hebt gewijzigd en je wilt dat de wijzigingen worden herkend:

```bash
rehash
```

## Tips
- Gebruik `rehash` regelmatig als je vaak nieuwe programma's of scripts toevoegt aan je systeem.
- Het is een goed idee om `rehash` uit te voeren na het installeren van software via een pakketbeheerder.
- Als je een foutmelding krijgt dat een commando niet gevonden kan worden, kan het helpen om `rehash` uit te voeren om de cache bij te werken.