# [Linux] C Shell (csh) docker-compose gebruik: Beheer van multi-container Docker-applicaties

## Overzicht
De `docker-compose` opdracht is een hulpmiddel dat wordt gebruikt om multi-container Docker-applicaties te definiëren en te beheren. Met `docker-compose` kun je eenvoudig een applicatie opzetten met meerdere services, netwerken en volumes, allemaal gedefinieerd in een enkele YAML-configuratiebestand.

## Gebruik
De basis syntaxis van de `docker-compose` opdracht is als volgt:

```bash
docker-compose [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties voor `docker-compose`:

- `up`: Start de gedefinieerde services.
- `down`: Stop en verwijder de services.
- `build`: Bouw de services zoals gedefinieerd in het `docker-compose.yml` bestand.
- `logs`: Toon de logs van de services.
- `ps`: Lijst de actieve containers van de gedefinieerde services.

## Veelvoorkomende Voorbeelden

### Starten van de applicatie
Om een applicatie te starten die is gedefinieerd in een `docker-compose.yml` bestand, gebruik je:

```bash
docker-compose up
```

### Stoppen van de applicatie
Om de applicatie te stoppen en de containers te verwijderen, gebruik je:

```bash
docker-compose down
```

### Bouwen van de services
Als je wijzigingen hebt aangebracht in de Dockerfile of de configuratie, kun je de services opnieuw bouwen met:

```bash
docker-compose build
```

### Bekijken van logs
Om de logs van alle services te bekijken, gebruik je:

```bash
docker-compose logs
```

### Lijst van actieve containers
Om een lijst van actieve containers te zien, gebruik je:

```bash
docker-compose ps
```

## Tips
- Zorg ervoor dat je een goed gestructureerd `docker-compose.yml` bestand hebt, zodat je eenvoudig je applicatie kunt beheren.
- Gebruik de optie `-d` met `docker-compose up` om de containers in de achtergrond te draaien.
- Maak gebruik van netwerken in je `docker-compose.yml` om de communicatie tussen containers te vergemakkelijken.
- Houd je `docker-compose.yml` bestand up-to-date met de laatste configuraties en afhankelijkheden voor een soepelere werking.