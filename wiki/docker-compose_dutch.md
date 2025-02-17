# [Linux] Bash docker-compose gebruik: Beheer van multi-container Docker-applicaties

## Overzicht
De `docker-compose` opdracht is een krachtige tool die het mogelijk maakt om multi-container Docker-applicaties te definiëren en te beheren. Met `docker-compose` kun je eenvoudig de configuratie van je containers in een YAML-bestand vastleggen en deze containers met één enkele opdracht opstarten, stoppen of beheren.

## Gebruik
De basis syntaxis van de `docker-compose` opdracht is als volgt:

```bash
docker-compose [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties die je kunt gebruiken met `docker-compose`:

- `up`: Start de gedefinieerde containers.
- `down`: Stop en verwijder de containers, netwerken en volumes die zijn gedefinieerd in het bestand.
- `build`: Bouw de services zoals gedefinieerd in het `docker-compose.yml` bestand.
- `logs`: Toon de logs van de containers.
- `exec`: Voer een commando uit in een draaiende container.

## Veelvoorkomende Voorbeelden

### Starten van de containers
Om de containers te starten die zijn gedefinieerd in het `docker-compose.yml` bestand, gebruik je:

```bash
docker-compose up
```

### Stoppen en verwijderen van containers
Om de containers te stoppen en te verwijderen, gebruik je:

```bash
docker-compose down
```

### Bouw de services
Als je wijzigingen hebt aangebracht in de Dockerfile of in de configuratie, kun je de services opnieuw bouwen met:

```bash
docker-compose build
```

### Toegang tot logs
Om de logs van de containers te bekijken, gebruik je:

```bash
docker-compose logs
```

### Voer een commando uit in een container
Als je een commando wilt uitvoeren in een specifieke container, bijvoorbeeld een bash-shell, gebruik je:

```bash
docker-compose exec <service_naam> bash
```

Vervang `<service_naam>` door de naam van de service zoals gedefinieerd in je `docker-compose.yml`.

## Tips
- Zorg ervoor dat je een goed gestructureerd `docker-compose.yml` bestand hebt, zodat je eenvoudig je containers kunt beheren.
- Gebruik de optie `-d` met `docker-compose up` om de containers in de achtergrond te draaien.
- Maak gebruik van netwerken in je `docker-compose.yml` om de communicatie tussen containers te vergemakkelijken.
- Houd je Docker- en Docker Compose-versies up-to-date voor de beste prestaties en beveiliging.